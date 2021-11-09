# Byte Order
### Source: https://beej.us/guide/bgnet/pdf/bgnet_usl_c_1.pdf Section 3.2
***
### SYNOPSIS:
 
- Intel or Intel-compatible processor = Little Endian

- Network Byte Order = Big-Endian 

- Endianness example using hex number b34f:
  -   Big-Endian:  b3 4f  
  
  | MSB|LSB|
|:--:|:--:|
| b3 |4f|
  - Little-Endian:  4f b3
  
  | MSB|LSB|
|:--:|:--:|
| b3 |4f|
 
- Your computer stores numbers in Host Byte Order. 

-  Assume the Host Byte Order isn’t right

-  Always run the value through a
function to set it to Network Byte Order

- The function will do the byte oder conversion if it has to.

- There are two types of numbers that you can convert: short (two bytes) and long (four bytes).

- ### IMPORTANT:
  
  -  Convert the numbers to Network Byte Order before they go out on the wire.
  
  -  Convert the numbers to Host Byte Order as they come in off the wire. 
  
- Use the following fuctions to make the appropriate conversion.
     
|Function|Description           |
|:------:|:--------------------:|
|htons() | host to network short|
|htonl() | host to network long |
|ntohs() | network to host short|
|ntohl() | network to host long |

