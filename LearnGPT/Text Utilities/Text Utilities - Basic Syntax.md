# Basic Syntax

The basic syntax for using a command-line tool consists of the command name followed by one or more arguments or options. An argument is a variable that provides a specific value to a command, while an option is a flag that modifies the behavior of a command. Usually, options are indicated by a hyphen (-) or double hyphen (--).

Here is an example of a basic command:

```
ls -l
```

This command lists the files and directories in the current directory in a long format.

## Common Command-Line Tools

Here are some of the most frequently used command-line tools:

- **cd**: Changes the current directory.
- **ls**: Lists files and directories.
- **cat**: Concatenates files or displays them on the screen.
- **mv**: Moves or renames files and directories.
- **cp**: Copies files and directories.
- **rm**: Removes files and directories.
- **mkdir**: Creates a new directory.
- **rmdir**: Deletes a directory.
- **grep**: Searches for a pattern in a file or files.
- **sed**: Edits a file or stream.
- **awk**: Filters and processes text files.

## Example Usage

Here are some examples of how these command-line tools can be used:

```
cd ~/Documents
```

Changes the current directory to the Documents folder in the user's home directory.

```
ls -la
```

Lists all files and directories in the current directory in a long format, including hidden files.

```
cat file.txt
```

Displays the contents of the file.txt file on the screen.

```
mv file.txt newfile.txt
```

Renames the file.txt file to newfile.txt.

```
cp file.txt ~/Documents/
```

Copies the file.txt file to the Documents folder in the user's home directory.

```
rm file.txt
```

Deletes the file.txt file.

```
mkdir newfolder
```

Creates a new folder named newfolder in the current directory.

```
rmdir newfolder
```

Deletes the newfolder directory if it is empty.

```
grep "example" file.txt
```

Finds all occurrences of the word "example" in the file.txt file.

```
sed 's/old/new/' file.txt
```

Replaces all occurrences of the word "old" with "new" in the file.txt file.

```
ls | awk '{print $1}'
```

Lists all files and directories in the current directory, displaying only the first column of output (the file/directory names).
