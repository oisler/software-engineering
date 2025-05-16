# Linux

A minimal list of useful Linux commands

## Create Directories
Create multiple directories at once.<br> 
The -p flag also creates parent directories if they don't exist.
```bash
mkdir -p git dir1 dir2 dir3
```

## Create Files
Create a new empty file (markdown in this example).
```bash
touch dir/file.md
```

## Remove File or Directory
Delete a file or directory.<br>
Use -r for recursive deletion (e.g. for folders).<br>
Use -f to force deletion without prompt.<br>
```bash
rm file.md
rm -rf folder/
```

## Rename or move Files
Rename a file, or move it to another location.
```bash
mv oldname.md newname.md
mv file.md folder/
```