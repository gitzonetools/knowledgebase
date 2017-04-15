# Linux Commands
## Filesystem Operations
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

```sh
cp [file to copy] [directory to copy into]
```

you can add various options. A few of them are:

```sh
-n // does prevent overwriting a file
-s // creates a symbolic link instead of copying the file
```

### SymLink
To symlink a directory, type the following

```sh
sudo ln -s /pathtofolder1/child/ /pathtofolder2/parent/
```

>#### Note:
**if parent folder exists** then symlink of
`/pathtofolder2/parent/child/`  
points to  
`/pathtofolder1/child`

>**if parent folder does not exist** then symlink of  
`pathtofolder2/parent/`  
points to  
`pathtofolder1/child`