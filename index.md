Welcome to My prodect Website Pages

目录

### Self-introduction

- I'm Qing Gao, a student from SMU. This page is used to display the learning results of smu7345. Through this course, I achieved:

1. Understand the differences between C + + and JS in operation.
2. Master the basic principle of network communication.
3. Utilize Emscripten to convert a c++ library/application into a web application via WebAssembly (WASM)
4. Package the web into a local app.



### Achievement display

#### Lab one 

> Building and Analyzing an Emscripten Library / Application

- If you want to download the complete lab code and report, click git connection···

1. #####  Setup the Emscripten pipeline 

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

   ![image-20211212093119262](https://tva1.sinaimg.cn/large/008i3skNgy1gxasoar1t1j31z40dgq6d.jpg)

- **Now you have already install the Emscripten successfully!~**

- **If you want to get more information about emscripten, please visit the [Emscripten](https://emscripten.org/) official website** 

  



2. ##### Verify with hello world project

   1. Create c++ file

   ```c++
   int main(int argc, char ** argv) {
     printf("Hello World\n");
   }
   ```

   

   2. Run `emcc hello.c -s WASH=1 -o hello.html`

   >Error: ‘zsh command not found: emcc’
   >
   >Reason: EMCC is not configured in the current path
   >
   >Solution：Put the hello.c file into emsdk file, and active the emcc

   a. Enter emsdk file environment, and activate environment variable

   ![image-20211212093640106](https://tva1.sinaimg.cn/large/008i3skNgy1gxastu4474j31z405gab2.jpg)

   b. Go back to the file path where hello.c is located, and run

   ![image-20211212093649718](https://tva1.sinaimg.cn/large/008i3skNgy1gxastyypdhj31z402idgb.jpg)

   c. File generated successfully

   ![image-20211212093658950](https://tva1.sinaimg.cn/large/008i3skNgy1gxasu58a5sj31gw0u0wgi.jpg)

   d. Open file with browser

   ![image-20211212093712458](https://tva1.sinaimg.cn/large/008i3skNgy1gxasudivabj31z40nkt9y.jpg)



3. ##### Compare and Contrast execution time between native and wasm based code bases

- This figure shows the running time of C + + code and converted code

![image-20211212094424657](https://tva1.sinaimg.cn/large/008i3skNgy1gxat1vhaj4j31z407qdhe.jpg)

- These two figures show the analysis of data after many experiments

![截屏2021-12-12 上午9.47.22](https://tva1.sinaimg.cn/large/008i3skNgy1gxat59aauvj31bc0sidl1.jpg)







#### Lab Two

> Building a JS library using WebIDL and Emscripten

- If you want to download the complete lab code and report, click git connection···

