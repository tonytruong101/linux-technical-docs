## Technical Overview

Nl is a command-line utility that is used to number the lines of a file or stream of text. It is commonly used for tasks such as creating numbered lists, adding line numbers to source code, and generating line numbering for documents.

**Here is a technical overview of how Nl works**:

1. Nl reads input from one or more files or standard input (stdin). The input is divided into lines, which are typically separated by a newline character.

1. Nl processes each line of input and adds a line number to the beginning of the line. By default, Nl starts numbering at line 1 and increments the line number by 1 for each line.

1. Nl provides a number of options that can be used to modify its behavior, such as -b (specify the numbering format), -n (set the starting line number and increment), and -w (set the number width).

After adding line numbers to the input lines, Nl prints the output to standard output (stdout) or writes it to a file.


## Nl Options & What do they do

list of some common options that can be used with nl:

- **-b**: Specify the type of lines to be numbered. Possible values are a (number all lines), t (number only non-empty lines), and n (number only lines that contain a non-space character).
- **-n**: Specify the numbering format. Possible values are ln (left-justified, no leading zeroes), rn (right-justified, no leading zeroes), lnz (left-justified, leading zeroes), and rnz (right-justified, leading zeroes).
- **-w**: Specify the width of the line number.


**Simple example of a Nl command that numbers the lines of a file**:

```
nl input.txt
```
This command reads the input file and adds line numbers to the beginning of each line. The resulting output consists of numbered lines.

**Example -b and -n options to number only non-empty lines and use a right-justified, no leading zeroes numbering format:**

```
nl -b t -n rn file.txt
```
This will number only the non-empty lines of file.txt using a right-justified, no leading zeroes numbering format.

**Example -w option to specify the width of the line number:**

```
nl -w 4 file.txt
```
This will number the lines of file.txt using a line number width of 4 characters.


## More Use Case Examples with Nl

**Number the lines of standard input**: 

nl can be used to number the lines of standard input, allowing you to use it in a pipeline with other commands. For example, to number the lines of the output of the ls command:

```
ls | nl
```

**Number the lines of a file and write the output to a new file**: 

nl can be used to number the lines of a file and write the output to a new file by redirecting the output of nl to a new file. For example:

```
nl file.txt > numberedfile.txt
```

**Number the lines of a file starting from a specific number**: 

nl can be used to specify the starting line number using the -n option. For example, to start numbering the lines of a file from 100:

```
nl -n 100 file.txt
```

**Number the lines of a file using a specific numbering format**: 

nl can be used to specify the numbering format using the -b option. For example, to number the lines of a file using Roman numerals:

```
nl -b roman file.txt
```


