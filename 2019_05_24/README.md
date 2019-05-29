# Lenguaje C-Iniciacion 

En esta clase se realizó una rápida revisión de un programa sencillo en C que imprime el mensaje "hola mundo".
Después se mostró la forma como se genera una librería de enlace estático y como la funcionalidad implementada en esta es invocada desde un programa en C.

### Se desarrollaron tres programas:

- [basico.c](https://github.com/SanMejia/SistemasOperativos/blob/master/2019_05_24/basico.c)
- [libfun.c](https://github.com/SanMejia/SistemasOperativos/blob/master/2019_05_24/libfun.c)
- [libfun.h](https://github.com/SanMejia/SistemasOperativos/blob/master/2019_05_24/libfun.h)

### Para compilar el programa se llevan a cabo los siguientes pasos:

- Generar la libreria

```
gcc -c libfun.c -o libfun.o
ar rcs libfun.a libfun.o

```

- En el paso anterior se generó el archivo ``` libfun.a ``` . Ahora enlazaremos el programa ``` basico.c ``` con la librería ``` libfun.a ``` .

```
gcc basico.c -L. -lfun -o basico

```

- Finalmente, el programa se ejecuta:

```

./basico

```
