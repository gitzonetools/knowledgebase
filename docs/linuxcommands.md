# Linux Commands
## Fileoperations
This section covers the basics of standard file operations within Linux.

### Create, Copy, Move, Delete

#### Create
Create a new textfile (html, jade, sass, coffee, javascript all are text-files):
```
nano [name of your new text file]
# note we are using nano for this
```
#### Copy
Copy a file:
```
cp [file to copy] [directory to copy into]
```
you can add various options. A few of them are:
```
-n // does prevent overwriting a file
-s // creates a symbolic link instead of copying the file
```
