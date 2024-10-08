## C Preprocessor and C Compiler
### 1. How to compile a C Program?
![](https://evolved-cpp.netlify.app/assets/img/the_compilation_process.fcb3cc6e.png)

### 2. Static Lib and Shared Lib different?
![](https://ismuniv.com/wp-content/uploads/2020/03/Static-Vs-Shared-Libraries.png)

Static library is linked into the program at compile time which means there is no additional run-time loading costs. Although it is added on app binaries size, it is able to ensure dependencies of the libraries are able to be met. Example with staticlib.a :
```bash
$ gcc main.o -o main staticlib.a
```

![Static lib](https://sesamenotes.wordpress.com/wp-content/uploads/2015/03/screen-shot-2015-03-28-at-1-46-54-pm.png?w=984&h=712)

Dynamic library can be loaded or unloaded its code at run-time. A program using a dynamic library only makes reference to code that it uses in the dynamic library. Example:
```sh
$ gcc -shared liba.o libb.o -o libtest.so
$ gcc main.c -o main -L -ltest
```

![](https://sesamenotes.wordpress.com/wp-content/uploads/2015/03/screen-shot-2015-03-28-at-1-47-03-pm.png?w=984&h=648)

