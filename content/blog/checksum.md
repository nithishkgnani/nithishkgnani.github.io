---
title: "Checksum calculation in UDP/IPv4 datagrams"
date: 2023-11-29
author: "Nithish K Gnani"
draft: false
---

There was a mismatch between the UDP checksum in the source and destination hosts while doing an experiment in the [TSN](/project/tsn/) project. To debug it I had to understand how the checksum is calculated in UDP/IPv4 datagrams. This blog post is my notes on this topic. I had a hard time finding a good resource on this topic online. I hope this helps someone.

## Definition

Checksum is the 16-bit one's complement of the one's complement sum of a
pseudo header of information from the IP header, the UDP header, and the
data,  padded  with zero octets  at the end (if  necessary)  to  make  a
multiple of two octets.  
Source: [RFC 768](https://datatracker.ietf.org/doc/html/rfc768)

## Fields used

The checksum calculation includes a pseudo header from the IP layer which contains source IP, destination IP, reserved (set to zero), protocol (set to the value representing UDP (0x11)), and UDP length fields. The UDP layer includes the UDP header and data. 
The fields used in computing the checksum for UDP/IPv4 datagrams are given in the following image:

{{< figure src="/img/other_images/UDP-checksum-fields.png" caption="Fields used in computing the checksum for UDP/IPv4 datagrams" >}}

At the source, while computing the checksum, the checksum field is set to zero. The checksum is computed over the entire UDP datagram, including the UDP header and data. A pseudo header is also included, with parts of IPv4 header fields. 

## Steps to calculate the UDP checksum:

1. **Divide the payload and headers into 16-bit words**: The payload and some of the headers (including some IP headers) are all divided into 16-bit words.

2. **Sum the 16-bit words**: These words are then added together. Whenever one of those additions results in a carry, the value is wrapped around and you add one to the value again.

3. **Handle overflow**: Wrapping any overflow around. This effectively takes the carry bit of the 16-bit addition and adds it to the value.

4. **Take the one's complement**: Lastly, the one’s complement of the resultant sum is taken. A one's complement sum is performed on all the 16-bit values then the one's complement (i.e., invert all bits) is taken of that value to populate the checksum field (with the extra condition that a calculated checksum of zero will be changed into all one-bits).

5. **Append the checksum to the message**: The result is appended to the message as the checksum.

At the receiving end, all the 16-bit words of the headers plus data area are added together (wrapping at 16 bits) and the result is checked against 0xffff. If the result is 0xffff, then the segment is valid else the segment has an error.

## Example

Let's take an example with the following hexadecimal values:  
*(This is a simplified example and actual UDP packets will have more data)*

```markdown
84eb dfea 9edf
```

Here's how you calculate the checksum:

1. **Divide the payload and headers into 16-bit words**:

    ```markdown
    84eb, dfea, 9edf
    ```

2. **Sum the 16-bit words**:

    ```markdown
    84eb
    +dfea
    +9edf
    ------
    =203b4
    ```

3. **Handle overflow**: There's an overflow since the sum `203b4` is more than `FFFF` (16 bits in binary). So, we wrap the overflow (2 in **2**03b4)  around:

    ```markdown
    03b4
    +   2
    ------
    =03b6
    ```

4. **Take the one's complement**: The one's complement of `3B6` is `FC49`.  

    ```markdown
                03B6 = 0000001110110110  
    One's complement = 1111110001001001 = FC49
    ```

5. **Insert the checksum to the datagram**: The checksum `FC49` is added to the checksum field of the UDP header.

At the receiving end, all the 16-bit words of the headers plus data area are added together (wrapping at 16 bits) and the result is checked against `FFFF`. If the result is `FFFF`, then the segment is valid else the segment has an error.


## Python script to calculate the checksum

The python script can be found in my [GitHub repository](https://github.com/nithishkgnani/Code-For-Fun/blob/main/Checksum.py).  
The program computes the checksum of a hexadecimal number input.  

1. Capturing a UDP packet in Wireshark and save its hexdump.
2. Choose the correct header fields and data from the packet as shown in [Fields used](#fields-used)
3. Make it single string to get the hexadecimal number
4. Run the below Python script and input the hexadecimal number

The steps done in the script are:  

1. Split the hexadecimal number into 4-bit chunks and pad the leftmost chunk with zeros if necessary
2. Split the number into 16-bit chunks (len of hex number = 4) and perform sum of the hexadecimal numbers
3. If there's a carry beyond 16 bits (len of sum > 4), repeat steps 1 & 2
4. Convert the hexadecimal sum to binary and do one's complement
5. The result is the checksum
