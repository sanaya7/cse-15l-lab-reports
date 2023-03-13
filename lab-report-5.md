# Lab Report - 5
Command chosen: find\
The find command, as the name implies, is used to find things. It allows users to search for files and directories based on various criteria, such as file names, permissions, sizes, and modification times. The find command can search for files and directories recursively in a given directory and its subdirectories, making it useful for managing and organizing large directory structures.

The syntax is: `find [path] [expression]`

*__Path__*: The directory to start the search from. If not specified, the search starts from the current directory.\
*__Expression__*: The set of criteria used to filter the files and directories. It can include various options, tests, and actions.

## 1. `-name`
The `-name` command is used when you know the name of a file but can't remember where you saved it.

```
[cs15lwi23aho@ieng6-203]:skill-demo1-data:339$ find . -name '*.txt'
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Abernathy/ch6.txt
./written_2/non-fiction/OUP/Abernathy/ch7.txt
./written_2/non-fiction/OUP/Abernathy/ch8.txt
./written_2/non-fiction/OUP/Abernathy/ch9.txt
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch1.txt
…
./written_2/skill-demo1-data/written_2/skill-demo1-data/written_2/skill-demo1-data/written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
./written_2/skill-demo1-data/results.txt
./results.txt
./grep-results.txt
./rsults.txt
```
