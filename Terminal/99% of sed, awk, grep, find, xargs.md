awk:  
* Awk is an entire programming language, but you usually just use it to print out a chunk of whitespace-separated text (linewise)  
  
```  
echo 'hello world' | awk '{ print $2 }'  
```  
  
* You can print out multiple things:  
  
```  
echo '2023-02-27 cool-srvr HTTP/2.0 GET /all_the_things' | awk '{ print $1, $4, $5 }'  
```  
  
grep:  
* Search for text  
  
```  
(echo 'hello'; echo 'world') | grep orld  
```  
  
* Negated with -v  
  
```  
(echo 'hello'; echo 'world') | grep -v orld  
```  
  
* Regexp with -E  
  
```  
(echo 'hello'; echo 'world') | grep -E '^h'  
```  
  
sed:  
* Full-featured stream editor  
  
* Substitute first instance of character (note: linewise):  
  
```  
(echo 'hello'; echo 'world') | sed 's/l/_/'  
```  
  
* Substitute instances of characters globally   
  
```  
(echo 'hello'; echo 'world') | sed 's/l/_/g'  
```  
  
find:  
* (I don't use this frequently but...)  
* Recursively list files by extension:  
  
```  
find . -name *.go  
```  
  
xargs:  
* Reads stdin and passes as args to subcommands  
  
* Split stdin and call echo each time with 1 arg:  
  
```  
(echo 'hello world'; echo 'hi mom') | xargs -n 1 echo  
```  
  
* Split stdin and call echo each time with pairs of args:  
  
```  
(echo 'hello world'; echo 'hi mom') | xargs -n 2 echo  
```  
  
* -I{} sets up a replacement where the arg is substituted into `{}` of the subcommand (see the OP comment)  
  
* Example: Open up all search results in vim (rg is one of many grep replacements). `rg -l` gives a list of filenames; convert those into `nvim <file1> <file2> ...`. `-o` fixes a quirky bug related to tty's  
  
```  
rg method_i_want_to_rename -l | xargs -o nvim  
```

- The `ripgrep -l` command is used to list only the files that match the given pattern, without displaying the actual matching lines

- The `xargs -o` command is used to control how `xargs` reads the input from the standard input (stdin).  By default, `xargs` reads items from stdin separated by whitespace (spaces, tabs, or newlines), and it treats quotes and backslashes as special characters. However, when used with the `-o` option, `xargs` treats each line of input as a separate item, regardless of whitespace or special characters.