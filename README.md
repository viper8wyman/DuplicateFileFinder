# DuplicateFileFinder
## Purpose: Find duplicate files across a Windows directory tree (to clean up my iPhone photo dumps)

This is a VERY rudimentary, single file Java app that searches through a directory hierarchy starting at the specified root and traversing down the tree. 

## Command-line arguments
1 (argv[0]) - full directory path
2 (argv[1]) - name of file to place only duplicate names/paths in (doesn't record first instance of a filename)
3 (argv[2]) - names of files that match "exactly" (see below); tab-separated

## Process
Code checks names of files first. 
If the code finds a match, it generates a hash for each file and compares.
If the hash (MessageDigest) is the same for each, it grabs length and last modification date.
If THOSE match, it writes the output to the specified output directory.
