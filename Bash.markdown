# Bash


### Change file permision in Unix using chmod.
In a terminal do
```
chmod 755 filename
```
to change the permission to read-write-execute for user, read-write for group and read-write for world. See other examples in the table.
```
User    Group    World    
r+w+x    r+w+x    r+w+x    
4+2+1    4+2+1    4+2+1    777
r+w+x    r+x    r+x    
4+2+1    4+0+1    4+0+1    755
r+w+x    r    r    
4+2+1    4+0+0    4+0+0    744
r    r+w    r+w+x    
4+0+0    4+2+0    4+2+1    467
```
### Change the user and/or group ownership of a given file or directory in Unix.
```
chown options owner-user:owner-group file
```
Example:
```
chown -R nur:minerva work
```
Changed the owner of the directory "work" recurcievely. The user is changed to "nur" with group "minerva". You have to login as root to do these changes.

### Make multiple directories with one command.
```
mkdir {dir1,dir2,dir3}
```
Usage: Create directories dir1, dir2, and dir3.

### Check environment variable is defined
```
# use the string "is not null" operator
if [ -n $MY_ENV_VAR ]; then
echo "MY_ENV_VAR is defined as $MY_ENV_VAR"
else
echo "MY_ENV_VAR is not defined."
fi 
```

### Check environment variable is not defined
```
# use the string "is null" operator
if [ -z $MY_ENV_VAR ]; then
echo "MY_ENV_VAR is not defined."
else
echo "MY_ENV_VAR is defined as $MY_ENV_VAR"
fi 
```

### Check available commands/aliases/etc.

`compgen` is a built-in bash command that can list all the Linux commands
you can run.

* `compgen -b` - show all the Bash builtins
* `compgen -k` - show all the Bash keywords
* `compgen -c` - show all the available commands
* `compegn -a` - show all the aliases
* `compgen -A function` - show all the Bash functions

### Loops on the command line
```
$ for f in `ls -1 /data/playlists/data*`; do  basename $f; done
```
