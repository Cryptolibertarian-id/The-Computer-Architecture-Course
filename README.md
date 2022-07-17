# The Computer-Architecture Course

 Learning Path to Learn Computer Architecture | With Gun



## Stack & Heap

A Program need memory to run, when a program is running, data must be stored in a **RAM** (Random Access Memory). Inside a running program there are two areas of memory that are used, namely the stack and the heap. Stacks and heaps are just ways of organizing RAM. The RAM itself is just a huge array of bytes.

Stack is used to make **Static Memory allocation** and Heap is used to create **Dynamic Memory allocation**, both of which are stored in RAM (Random Access Memory).

1. Variables allocated on the stack are stored directly in memory and access to static memory is very fast. 
2. Variables allocated on the heap have memory allocated at run time and access to dynamic memory tends to be slow.

The heap is a more flexible data structure in that memory can be allocated and freed from the heap in any order desired. It is not limited to LIFO. When you need data to exist in a pattern which can't be described by LIFO, you need something like a heap. 

Another factor which plays into whether a piece of data goes on the heap or the stack, is whether the size of that data is known at compile time.



---



## Memory

Memory

1. Buffer Memory
2. Cache Memory



## Buffer Memory

A buffer is a piece of memory used to store something. **Buffer memory** are memory spaces that are used to store data temporarily within **Dynamic Random Access Memory (RAM)**. CPU can store data temporarily, like the data to be forwarded to other slow speed output devices or other secondary storage devices, to enable the computer to execute other processes. It is implemented to match the speed of slow IO devices with processor. It stores or holds the actual copy of data.



### Node.js Example

[Buffers](http://nodejs.org/docs/latest/api/buffer.html) can be used for taking a string or piece of data and doing Base64 encoding of the result. 

For example encoding string to base64 string:

```javascript
> console.log(Buffer.from("Hello World").toString('base64'));
SGVsbG8gV29ybGQ=
```

 This is an encoding to ASCII string :

```javascript
> console.log(Buffer.from("SGVsbG8gV29ybGQ=", 'base64').toString('ascii'))
Hello World
```

In Node.js or browser, Buffers are a global object, so no require is needed. Buffers created with strings can take an optional encoding parameter to specify what encoding the string is in. The available `toString` and `Buffer` constructor encodings are as follows:

- 'ascii' - for 7 bit ASCII data only. This encoding method is very fast, and will strip the high bit if set.
- 'utf8' - Multi byte encoded Unicode characters. Many web pages and other document formats use UTF-8.
- 'ucs2' - 2-bytes, little endian encoded Unicode characters. It can encode only BMP(Basic Multilingual Plane, U+0000 - U+FFFF).
- 'base64' - Base64 string encoding.



## Cache Memory

**Cache memory** spaces that are used to store data temporarily within high-speed memory **Static Random Access Memory (RAM)**. Cache are accessed frequently by processes to get faster Information that is used and accessed by most of the programs.   Cache are implemented to reduce the access time and improve the latency time of the frequently used data. The cache holds the copy of original data.   