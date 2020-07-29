# SMALL LINUX SHELL
### By Filipe Chagas

A small Linux command interpreter implemented using the kernel syscall interface. It was done for a college exam that has already happened.



## Syntax 
* No arguments:	[command]
* Single argument:	[command] [arg]
* Two arguments:	[command] [arg_0] [arg_1]
* _N_ arguments:	[command] [arg_0] [arg_1] ... [arg_{N-1}]

## Basic commands

| Command | Arguments | Description | Usage Example |
|---------|-----------|-------------|---------|
| **help**    |           | Print informations about the shell. | help |
| **pwd**     |           | Print current working directory path. | pwd |
| **cd**      | destination_path  | Change working directory path. | cd /home |
| **ls**      | path _(optional)_ | Lists entries in the directory (argument directory or working directory). | ls |
| **exec** | path, \[arg\_1 , ... , arg\_n\] _(optional)_| Execute the _path_ file. | exec echo hello |
| **exit**    |           | Close the shell. | exit |
| **print**   | text, ..., text | Print texts |

## Commands with variables

| Command Line | Description |
|--------------|-------------|
| **set** destvar **as** text | Define a variable named 'destvar' and make the text its content. |
| **set** destvar **like** originvar | Define a variable named 'destvar' and make the content of the 'originvar' variable its content (by copy).|
| **print** $varname | Print the content of 'varname' variable. |
| **print** $$varname | Print '$varname' (double '$' means that '$varname' is not a variable). |
| **uv** command $varname |  Perform the command with variables as arguments |

**IMPORTANT**: Variable's names must have only alphabetical lowercase characters. 

### Examples

Define a variable named 'homedir' as '/home' and use it with the **cd** command:
```
>>> set homedir as /home
>>> uv cd $homedir
>>> pwd
/home
```

Define two variables, 'name' and 'surname', and use them to print 'My name is Filipe Chagas': 
```
>>> set name as Filipe
>>> set surname as Chagas
>>> print My name is $name $surname
My name is Filipe Chagas 
```

Define three variables with the same content:
```
>>> set one as hello_world
>>> set two like one
>>> set three like two
>>> print $one $two $three
hello_world hello_world hello_world 
```

## Building

It's very very simple. Just use the following command:

```
gcc main.c -o smallshell
```

I developed this using GCC version 9.3.0.


