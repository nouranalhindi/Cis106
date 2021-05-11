#  Creating directories
**The mkdir command**
* mkdir is used for creating a single directory or multiple directories.
* To create a directory with mkdir type: mkdir + the name of the directory.
* To create multiple directories, separate each directory name with a space.
* You can create directories in the present working directory or in a different directory by using
an absolute path or relative path.
* You can create a directory with a space in its name using the escape character (\) or by
surrounding the name in quotation marks (‘ ‘ or “ ” ).
* If you try to create a directory that already exists, you will get an error notifying you that the file
already exists.
### Creating Files 
  **The touch command**
*  touch is used for creating files
###  Deleting files and directories
 **The rm command**
* rm removes files.
* rm by default does not removes directories. To remove a directory use rm with the -r option.
* In Linux and other Nix systems you cannot remove non empty directories.
* To remove empty directories use the **rmdir** command.
###  Moving files and directories
 **The mv command**
* mv moves and renames directories.
* Where source is the file or directory that you want to move and
destination is where the directory or file is going.
* Both source and destination can be an absolute path or relative path
* The mv command has many useful options. However, this course focuses
on its two basic functionalities.
### Copying files and directories
 **The cp command**
* cp copies files/directories from a source to a destination
* Like the mv command the cp command has many options but in the
course we will limit it to its main function.

# Using wildcards
* Wildcard represents letters and characters used to specify a filename for searches.
* File globbing is the processing of pattern matching using wildcards.
* The wildcards are officially called metacharacter wildcards.
### The * Wildcard
* The main wildcard is a star, or asterisk (*) character.
* A star alone matches anything and nothing and matches any number of
characters.
### The ? Wildcard 
* The ? wildcard metacharacter matches **precisely one character**. You might need the question mark to minimize a long list of files names down to a few.
* In addition, the question mark proves very useful when working with hidden files (hidden files are also called dot files).
### The[ ] Wildcard
* The brackets wildcard match a single character in a range.
* The brackets wildcard use the exclamation mark to reverse the match. For example, match everything except
vowels [!aeiou] or any character except numbers [!0-9]
### Using Brace Expansion
* Brace expansion {} is not a wildcard but another feature of bash that allows you to generate arbitrary strings to use with commands.
* 