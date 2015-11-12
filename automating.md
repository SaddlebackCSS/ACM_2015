# Adding Automated Testing

You will be able to download the sample input/output for the problems in a ZIP file.
You can extract the files using the graphical file manager or the `unzip` command
(eg `unzip samples.zip`).
The sample input will be in a `.in` file, and the expected output will be in a similarly-named `.out` file.

You can redirect your program's stdin using the following:

```sh
./a.out < sample.in
```

You can compare your output to the expected output using the `sdiff` command:

```sh
./a.out < sample.in | sdiff -w80 /dev/stdin sample.out
```

This leads to the following script to recompile a program and test it against every sample in the current directory:

```sh
g++ *.cpp && for infile in *.in
do
    outfile=$(basename -s .in $infile).out
    echo $infile
    ./a.out < $infile | sdiff -w80 /dev/stdin $outfile
    echo
done
```

Save this in a `.sh` file (eg `retest.sh`) and run it using the `sh` command:

```sh
sh retest.sh
```

Alternatively, you can condense the entire script to one line and type it directly into the terminal **(note the semicolons)**:
```sh
g++ *.cpp && for infile in *.in ; do outfile=$(basename -s .in $infile).out ; echo $infile ; ./a.out < $infile | sdiff -w80 /dev/stdin $outfile ; echo ; done
```

After entering and running this command, use the up-arrow key to re-run it.

(note: These examples are for C++. See the `Compiling` page for Java commands)
