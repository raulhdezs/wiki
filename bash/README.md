# How to remove easily a selected list of files from a folder
1. Write all filenames in a text file `x` with `ls > x`
2. Remove from the text file `x` the files you want to keep using `vi x`
3. Remove all files in `x` with `rm $(< x)`
4. Remove `x` with `rm x`