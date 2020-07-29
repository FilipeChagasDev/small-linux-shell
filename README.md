# SMALL LINUX SHELL
### By Filipe Chagas

A small Linux command interpreter implemented using the kernel syscall interface. It was done for a college exam that has already happened.

## Syntax 
* No arguments:	[command]
* Single argument:	[command] [arg]
* Two arguments:	[command] [arg_0] [arg_1]
* _N_ arguments:	[command] [arg_0] [arg_1] ... [arg_{N-1}]

## Available commands

| Command | Arguments | Description |
|---------|-----------|-------------|
| help    |           | Print informations about the shell. |
| pwd     |           | Print current working directory path. |
| cd      | destination_path  | Change working directory path. |
| ls      | path _(optional)_ | Lists entries in the directory (argument directory or working directory). |
| exit    |           | Close the shell. |


