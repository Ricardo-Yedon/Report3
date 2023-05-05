Hi, for this assignment, I am investigating some of the interesting alternative ways to use find in terminal:

-#1-type

The -type option is used to search for files based on their type. It accepts the following arguments:

f: to search for regular files

d: to search for directories

l: to search for symbolic links

c: to search for character devices

b: to search for block devices

s: to search for sockets

p: to search for named pipes

Example 1: Search for all regular files under the ./technical directory:
```
$ find ./technical -type f
```
Example 2: Search for all directories under the ./technical directory:
```
$ find ./technical -type d
```
Source: https://linuxize.com/post/how-to-use-the-find-command-to-search-for-files-in-linux/

-#2-name
The -name option is used to search for files based on their name. It accepts a string argument representing the name pattern to search for.

Example 1: Search for all files under the ./technical directory with the name README.md:
```
$ find ./technical -name README.md
```
Example 2: Search for all files under the ./technical directory with the extension .py:
```
$ find ./technical -name "*.py"
```
Source: https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

-#3-size
The -size option is used to search for files based on their size. It accepts a size argument followed by a unit:

c: for bytes
k: for kilobytes
M: for megabytes
G: for gigabytes
+: for files larger than the specified size
-: for files smaller than the specified size
n: for files with exact size
Example 1: Search for all files under the ./technical directory that are larger than 1MB:
```
$ find ./technical -size +1M
```
Example 2: Search for all files under the ./technical directory that are smaller than 100 bytes:
```
$ find ./technical -size -100c
```
Source: https://linuxhandbook.com/find-command-examples/

-#4-mtime
The -mtime option is used to search for files based on their modification time. It accepts a number argument followed by a unit:

+n: for files modified more than n days ago
-n: for files modified less than n days ago
n: for files modified exactly n days ago
Example 1: Search for all files under the ./technical directory that were modified more than 7 days ago:
```
$ find ./technical -mtime +7
```
Example 2: Search for all files under the ./technical directory that were modified exactly 3 days ago:
```
$ find ./technical -mtime 3
```
Source: https://www.cyberciti.biz/faq/howto-finding-files-by-date/
