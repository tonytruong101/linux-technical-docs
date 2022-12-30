## Technical Overview
Wc is a command-line utility that is used to count the number of lines, words, and characters in a file or stream of text. It is commonly used for tasks such as counting the number of words in a document, finding the length of a file, and analyzing text data.

**Here is a technical overview of how Wc works**:

1. Wc reads input from one or more files or standard input (stdin). The input is divided into lines, which are typically separated by a newline character.

1. Wc processes each line of input and counts the number of lines, words, and characters. A word is typically defined as a sequence of non-whitespace characters.

1. Wc provides a number of options that can be used to modify its behavior, such as -l (count the number of lines), -w (count the number of words), and -m (count the number of characters).

After counting the input, Wc prints the results to standard output (stdout). By default, Wc prints the number of lines, words, and characters.


## wc Options & What they do

list of some common options that can be used with wc:

- **-c**: Count the number of bytes.
- **-l**: Count the number of lines.
- **-m**: Count the number of characters.
- **-w**: Count the number of words.

**Simple example of a Wc command that counts the number of lines in a file**:

```
wc -l input.txt
```
This command reads the input file and counts the number of lines. The resulting output consists of a single number that represents the total number of lines in the file.


**Example -l and -w options to count the number of lines and words in a file:**

```
wc -lw file.txt
```
This will count the number of lines and words in file.txt.

**Example -c and -m options to count the number of bytes and characters in a file:**

```
wc -cm file.txt
```
This will count the number of bytes and characters in file.txt.

## More Use Case Examples with Wc

**Display the word count of a file**: 

wc can be used to display the number of words in a file. You can specify the -w option to display only the word count. For example:

```
wc -w file.txt
```

**Display the byte count of a file**: 

wc can be used to display the number of bytes in a file. You can specify the -c option to display only the byte count. For example:

```
wc -c file.txt
```

**Display the line, word, and byte count of a file**: 

wc can be used to display the line, word, and byte count of a file by not specifying any options. For example:

```
wc file.txt
```

**Count the number of characters in a file**: 

wc can be used to count the number of characters in a file by specifying the -m option. For example:

```
wc -m file.txt
```

**Count the number of lines in a file**: 

wc can be used to count the number of lines in a file by specifying the -l option. For example:

```
wc -l file.txt
```
