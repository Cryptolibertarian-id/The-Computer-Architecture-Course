# The Computer-Architecture Course

 Learning Path to Learn Computer Architecture | With Gun



## Memory

Memory

1. Buffer Memory
2. Cache Memory



## Buffer Memory

Buffer memory are memory spaces that are used to store data temporarily within Dynamic Random Access Memory (RAM). CPU can store data temporarily, like the data to be forwarded to other slow speed output devices or other secondary storage devices, to enable the computer to execute other processes. It is implemented to match the speed of slow IO devices with processor.  It stores or holds the actual copy of data.



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

Cache memory spaces that are used to store data temporarily within high-speed memory Dynamic Random Access Memory (RAM). Cache are accessed frequently by processes to get faster Information that is used and accessed by most of the programs.   Cache are implemented to reduce the access time and improve the latency time of the frequently used data. The cache holds the copy of original data.   