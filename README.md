# Shell data processing:

## Steps:
- Create a folder.Right click on the folder and click on "Open PowerShell window here as administrator"
- Create subfolder named shell-data-processing 
```
mkdir shell-data-processing
```
- Change directory into subfolder
```
cd shell-data-processing
```
- Create a new empty file named README.md,.gitignore
```
ni README.md
ni .gitignore
```
- List the contents of current directory
```
ls
```
- Open the folder in VS code 
```
code .
```
- Use the curl command to return the page text and output to a file

```
curl "https://www.tutorialspoint.com/software_engineering/index.htm" -O "data.txt"

```
- Transform each space ' ' into a return character '\12' and redirect to specified file
```
tr ' ' '\12' < data.txt

```
- Pipe the output to sort
```
tr ' ' '\12' < data.txt | sort
```
- Pipe the sorted output to uniq -c to count
```
tr ' ' '\12' < returnedfile | sort | uniq -c
```
- Pipe the reduced output to sort with -nr flag
```
tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr

```
- Redirect the output to result.txt
```
tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr > result.txt
```

- Use the up arrow to get the previously used command
- Use the sort --help to get the options with descriptions

## Understanding Important Bash Commands:
- -n means numeric
- -r means reverse
- (>) means redirect
- (>>) means redirect and append
- Type ls to list the contents of the default directory. Send the result to a new file called temp.txt (ls > temp.txt). 
- Use the cat command to display the contents of temp.txt. 
- Copy in Bash is not CTRL+C as in Windows, instead use CTRL+SHIFT+C.

## Other important commands:
### Bash preview:
- cat filename (To get the contents of the file)
- head -10 filename.fx (To display the top 10 results of the file)
- tail -2 filename.fx (To display the botton 10 results of the file)
### PowerShell cat:
- Get-Content filename.fx (To get the contents of the file)
- gc one.txt -head 2 (To display the top 2 results of the file)
- gc one.txt -tail 2 (To display the bottom 2 results of the file)


