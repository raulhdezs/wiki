# Useful commands
## Remove easily a selected list of files from a folder
1. Write all filenames in a text file `x` with `ls > x`
2. Remove from the text file `x` the files you want to keep using `vi x`
3. Remove all files in `x` with `rm $(< x)`
4. Remove `x` with `rm x`

## Remove files created before mm/dd/yyyy hh:mm:ss
```bash
find . -type f ! -newermt 'mm/dd/yyyy hh:mm:ss' -exec rm -f {} \;
```
## Remove files contaning 'nan'
```bash
find path/to/directory -type f -exec egrep -Il 'nan' {} \; | xargs rm -fv
```
## Save program output into a text file
- Run program saving the output into a text file
```bash
./run > out.txt
```
- Run program saving the output + error messages
```bash
./run &> out.txt
```
- Run program saving the output + error messages into a file while showing them in console too
```bash
./run 2>&1 | tee out.txt
```
