## Technical Overview

Fmt is a command-line utility that is used to reformat and justify text. It is commonly used for tasks such as formatting text files, creating tables, and formatting text for printing.

**Here is a technical overview of how Fmt works**:

1. Fmt reads input from one or more files or standard input (stdin). The input is divided into lines, which are typically separated by a newline character.

1. Fmt processes each line of input and reformats it according to the specified options. By default, Fmt adjusts the line breaks and word wraps the text to fit within a specified line width, such as 75 or 80 characters.

1. Fmt provides a number of options that can be used to modify its behavior, such as -w (set the line width), -s (squeeze multiple adjacent blank lines into a single blank line), and -u (do not break lines at spaces).

After reformatting the input lines, Fmt prints the output to standard output (stdout) or writes it to a file.


## Fmt Options & What do they do

list of some common options that can be used with fmt:

- **-w**: Set the maximum line width.
- **-s**: Treat multiple spaces as a single space.
- **-t**: Make the first line of each paragraph flush with the left margin.
- **-p**: Indent the first line of each paragraph by the specified number of spaces.
- **-g**: Set the maximum line width and the width of the first line of each paragraph.


**Simple example of a Fmt command that reformats a file to fit within a 75-character line width**:

```
fmt -w 75 input.txt
```
This command reads the input file and reformats the lines to fit within a 75-character line width.

**Example -w option to set the maximum line width:**

```
fmt -w 60 file.txt
```
This will reformat the text in file.txt such that no line is longer than 60 characters.

**Example -s option to treat multiple spaces as a single space:**

```
fmt -s file.tx
```
This will reformat the text in file.txt such that multiple spaces are replaced with a single space.

**Example -w and -t options to set the maximum line width and make the first line of each paragraph flush with the left margin:**

```
fmt -w 60 -t file.txt
```
This will reformat the text in file.txt such that no line is longer than 60 characters and the first line of each paragraph is flush with the left margin.


## More Use Case Examples with Fmt

**Indent paragraphs**: 

fmt can be used to indent the first line of each paragraph in a file. For example:

```
fmt -i file.txt
```

**Adjust the spacing between words**: 

fmt can be used to adjust the spacing between words in a file. For example, to double the spacing between words:

```
fmt -s -2 file.txt
```

**Reformat text from standard input**: 

fmt can be used to reformat text from standard input, allowing you to use it in a pipeline with other commands. For example, to reformat the output of the ls command:

```
ls -l | fmt -w 80
```


