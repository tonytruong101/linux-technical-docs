## Technical Overview

Uniq is a command-line tool that is used to remove duplicate lines from a file or stream of text. It is commonly used for tasks such as deduplicating lists, counting the number of unique lines in a file, and comparing files for differences.

**Here is a technical overview of how Uniq works**:

1. Uniq reads input from one or more files or standard input (stdin). The input is divided into lines, which are typically separated by a newline character.

1. Uniq processes the input lines and compares adjacent lines to identify duplicates. By default, Uniq considers two lines to be duplicates if they are identical.

1. Uniq provides a number of options that can be used to modify its behavior, such as -c (count the number of occurrences of each line), -d (only print duplicate lines), -u (only print unique lines), and -i (ignore case).

After processing the input lines, Uniq prints the output to standard output (stdout) or writes it to a file.

## Uniq Options & What they do

list of some common options that can be used with uniq:

- **-c**: Precede each output line with a count of the number of times the line occurred in the input.
- **-d**: Only print duplicate lines, one for each group.
- **-i**: Ignore case when comparing lines.
- **-u**: Only print unique lines.

**Example -c option to precede each output line with a count of the number of times it occurred in the input:**

```
uniq -c file.txt
```
This will filter out adjacent, duplicate lines from file.txt and precede each output line with a count of the number of times it occurred in the input.

**Example -d option to only print duplicate lines, one for each group**:

```
uniq -d file.txt
```
This will filter out adjacent, duplicate lines from file.txt and only print the duplicate lines, one for each group.


## More Use Case Examples with Uniq

**Remove duplicate lines from a file**: 

uniq can be used to remove duplicate lines from a file and display the output on the terminal. For example:

```
uniq file.txt
```

**Display only duplicate lines in a file**: 

uniq can be used to display only the duplicate lines in a file by specifying the -d option. For example:

```
uniq -d file.txt
```

**Remove duplicate lines from standard input**: 

uniq can be used to remove duplicate lines from standard input, allowing you to use it in a pipeline with other commands. For example, to remove duplicate lines from the output of the ls command:

```
ls | uniq
```

**Ignore leading spaces when identifying duplicate lines**: 

uniq can be used to ignore leading spaces when identifying duplicate lines by specifying the -b option. For example:

```
uniq -b file.txt
```

**Ignore the first n fields when identifying duplicate lines**: 

uniq can be used to ignore the first n fields when identifying duplicate lines by specifying the -f option. For example, to ignore the first two fields:

```
uniq -f 2 file.txt
```
