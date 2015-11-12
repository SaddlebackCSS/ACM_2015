# Manually Compiling

If your preferred IDE is not functioning adequately, you may prefer using a basic text editor and the terminal.

The basic text editor can be found in the applications menu and is usually called `Text Editor` or `Leafpad`.

The graphical file manager usually has an option called `Open in Terminal`; check all of the menus
(including the right-click menu).
This way, the terminal will have already set the current directory to your project folder.

You can also open the terminal from the applications menu.
It is usually called `Terminal`, `xterm`, `uxterm`, or `Konsole`.

Use the following commands to navigate the terminal:

- `pwd` Print the *name* of the current directory (folder).
- `ls` Print the *contents* of the current directory.
- `cd [dir]` Change the current directory to `dir` (a subfolder of the *current* current folder).
- `cd ..` Change to the parent of the current directory

## Compiling and Running C++

C++ is compiled using the GNU C++ Compiler, which is called `g++`.
To compile all `.cpp` files in the current folder, use:

```sh
g++ *.cpp
```

This will create an executable called `a.out`.
To run the compiled program, use:

```sh
./a.out
```


## Compiling and Running Java

The Java compiler is called `javac`.
To compile all `.java` files in the current folder, use:

```sh
javac *.java
```

To run a Java program, you must give `java` the name of the class which contains
your `public static void main(String[] args)` method.
If the class containing this method is called `Main`, execute it using:

```sh
java Main
```

**(Note the lack of a `.java` or `.class` extension)**

## Notes

- The online judge might add additional command-line arguments to the submissions. Check your workstation and the online judge for any notes.
- If your program freezes, use `Ctrl-C` to terminate it.
- If your program reads to the end of stdin (eg if you are using `while(!cin.eof())` or `while(in.hasNext())`), use `Ctrl-D` to send the end-of-file and exit the loop.
- If you want to copy/paste in the terminal, use `Ctrl-Shift-C` and `Ctrl-Shift-V` (or the Edit menu).
