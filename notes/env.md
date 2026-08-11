# Text-Fu
## Tee Command: Used to split output.
```
ls | tee peanuts.txt
```
-> See the output of ls on the terminal. The contents of peanuts.txt will also be the same
* Can chain these commands:
```
ls -la /etc | tee etc_listing.txt | grep "conf"
```
- It lists the contents of the /etc directory, pipes that output to tee, which saves to etc_listing.txt and passes it along to grep to filter "conf"
## env
* The Linux system uses environment variables to store information that the shell and other processes can access.
* You can view the value of a specific variable by prefixing its name with a *$* symbol
```
echo $HOME
```
- This command will display the path to your home directory (/Users/minh)
```
echo $USER
```
- This will output your current username. Info is stored in your shell's environment.
```
echo $PATH 
```
- This command returns a colon-separated list of directories. When you type a command, your system searches through these directories to find the corresponding executable file.
## Command Substitution *$()*
* This allows you to take the output of a command and save it into a variable
```
TODAY=$(date +%Y-%m-%d)
echo "Today's date is $TODAY"
```
## Archiving with *tar*
* Compress a folder: tar -czvf backup.tar.gz /path/to/folder

    -c: Create archive

    -z: Compress using gzip

    -v: Verbose (show files being processed)

    -f: Specify filename

- The command clumps everything together into a .tar file, and then it compresses using gzip (which adds the .gz extension)
- Because -f requires the filename immediately after it, f must almost always be the last letter in your block of flags. Typing tar -cfzv archive.tar will fail, because it thinks the filename is zv.
* Extract an archive: tar -xzvf backup.tar.gz -C /path/to/destination