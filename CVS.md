# CVS



### Checkout
```
cvs co minervadoc/PB024_MLVertexFinding
```

### Update
Bring working dir specified up to date with the repository (merge changes made to the repository into the local files).
```
cvs update –dA package  
```
Bring just the named file up-to-date with the repository
```
cvs update –A filename
```
Do not change any files. Attempt to execute the cvs_command, but only to issue reports; do not remove, update, or merge any existing files, or create any new files.
```
cvs -n update -Af 
```

### Find history 

```
cvs history
```

### Import
```
cd ~/mydir/package
cvs import -m "First import with comment" file_or_dirctory_path version_number
```

### Structure

```
cvs <any command below> 

• Structure:          Overall structure of CVS commands
• Exit status:          Indicating CVS’s success or failure
• ~/.cvsrc:          Default options with the ~/.cvsrc file
• Global options:          Options you give to the left of cvs_command
• Common options:          Options you give to the right of cvs_command
• add:          Add files and directories to the repository
• admin:          Administration
• annotate:          What revision modified each line of a file?
• checkout:          Checkout sources for editing
• commit:          Check files into the repository
• diff:          Show differences between revisions
• export:          Export sources from CVS, similar to checkout
• history:          Show status of files and users
• import:          Import sources into CVS, using vendor branches
• log:          Show log messages for files
• rdiff:          ’patch’ format diffs between releases
• release:          Indicate that a directory is no longer in use
• remove:          Remove files from active development
• update:          Bring work tree in sync with repository
```
