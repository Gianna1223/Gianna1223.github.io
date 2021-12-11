## Welcome to My prodect Website Pages

目录

### Self-introduction

- I'm Qing Gao, a student from SMU. This page is used to display the learning results of smu7345. Through this course, I achieved:

1. Understand the differences between C + + and JS in operation.
2. Master the basic principle of network communication.
3. Have a preliminary understanding of emscrxxx and master some simple applications.
4. Package the web into a local app.

<5个lab的内容>

1. utilize Emscripten to convert a c++ library/application into a web application via WebAssembly (WASM)
2. 



### Achievement display

#### Lab one 

> Building and Analyzing an Emscripten Library / Application

- If you want to download the complete lab code and report, click [Here](https://github.com/Gianna1223/7345Labs.git)

1. Setup the Emscripten pipeline 

   1.  Download emsdk through git's clone command

   `git clone https://github.com/emscripten-core/emsdk.git`

   2.  Enter folder

   `cd emsdk`

   3.  Get the latest emsdk version

   `git pull`

   4. Download and install the latest tools

   `./emsdk install latest`

   5.  Activate tool

   `./emsdk active latest`

   6.  Run to see if the installation is successful

   `emcc -v`

- Now you have already install the Emscripten successfully!~
- If you want to get more information about emscripten, please visit the [Emscripten](https://emscripten.org/) official website



2. Verify with hello world project

   1. Create c++ file
   2. Run `emcc hello.c -s WASH=1 -o hello.html`

   >Error: ‘zsh command not found: emcc’
   >
   >Reason: EMCC is not configured in the current path
   >
   >Solution：Put the hello.c file into emsdk file, and active the emcc

   a. Enter emsdk file environment, and activate environment variable

   b. Go back to the file path where hello.c is located, and run

   c. File generated successfully

   d. Open file with browser

3. Compare and Contrast execution time between native and wasm based code bases

图 图 图



#### Lab Two

> Building a JS library using WebIDL and Emscripten

- If you want to download the complete lab code and report, click git connection···

This is a library lending sales statistics program, including library class and book class. Book class is used to store book information, and library class is used to store library management information. When a student borrows a book, the system will first judge whether there is this book and whether there is enough inventory of this book. If so, students need to pay the corresponding rent to terminate the contract, The program will count the total and average borrowing sales of the library.

