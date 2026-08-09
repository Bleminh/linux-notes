# Directing Traffic
1. The Overwrite (>):
Instead of printing to the screen, send the output to a file. If the file exists, this *ERASES* what was there and *REPLACES* it.
2. The Append (>>)
This adds to the bottom of a file without deleting the existing content.
3. The Pipe (|):
It takes the output of the left command and immediately feeds it as the input to the right command.
4. Search a file:
grep is a search tool. It looks for specific words or patterns inside text. Can be used with pipes.
```
df -h | grep "Data" (look at all drive data and filter those to only the main drive)
history | grep "git" (show every git commands recently run)
```