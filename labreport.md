Hi, for this assignment, I am investigating some of the interesting alternative ways to use find in terminal:

##1-type: This option is used to search for files of a specific type. The available file types are f (regular file), d (directory), l (symbolic link), c (character device), and b (block device). Here are two examples of using the -type option:

```
$ find ./technical -type d
./technical
./technical/programming_languages
./technical/operating_systems
./technical/databases

$ find ./technical -type f
./technical/programming_languages/python.txt
./technical/programming_languages/javascript.txt
./technical/operating_systems/linux.txt
./technical/databases/mysql.txt
```

This command searches for all directories in the ./technical directory and displays their paths. Similarly, it searches for all regular files in the ./technical directory and displays their paths.

Source: [[[Linuxize](https://linuxize.com/post/how-to-use-find-command-to-search-for-files-in-linux/)
](https://linuxize.com/post/how-to-use-find-command-to-search-for-files-in-linux/)](https://linuxize.com/post/how-to-use-find-command-to-search-for-files-in-linux/)

##2-iname: This option is used to search for files by name without case sensitivity. Here are two examples of using the -iname option:

```
$ find ./technical -iname "*LINUX*"
./technical/operating_systems/linux.txt

$ find ./technical -iname "*PY*"
./technical/programming_languages/python.txt
./technical/programming_languages/cpython.txt
```

This command searches for all files in the ./technical directory that contain the string "LINUX" in their name, regardless of case sensitivity. Similarly, it searches for all files in the ./technical directory that contain the string "PY" in their name, regardless of case sensitivity.

Source: [The Linux Handbook](https://linuxhandbook.com/find-command-examples/)

##3-size: This option is used to search for files of a specific size. The available size options are + (greater than), - (less than), and = (equal to). Here are two examples of using the -size option:

```
$ find ./technical -size +1M
./technical/programming_languages/javascript.txt

$ find ./technical -size -100k
./technical/programming_languages/cpython.txt
./technical/operating_systems/linux.txt
```

This command searches for all files in the ./technical directory that are larger than 1 megabyte and displays their paths. Similarly, it searches for all files in the ./technical directory that are smaller than 100 kilobytes and displays their paths.

Source: [TecMint](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)

##4-mtime: This option is used to search for files that were modified within a certain time frame. The available time frame options are + (more than), - (less than), and = (exact). Here are two examples of using the -mtime option:

```
$ find ./technical -mtime =7
./technical/programming_languages/python.txt

$ find ./technical -mtime -90 -type d
./technical
./technical/programming_languages
./technical/databases
```

This command searches for all files in the ./technical directory that were modified exactly 7 days ago and displays their paths. Similarly, it searches for all directories in the ./technical directory that were modified less than 90 days ago and displays their paths.

Source: [Computer Hope](https://www.computerhope.com/unix/ufind.htm)
