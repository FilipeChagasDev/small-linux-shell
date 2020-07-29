# SMALL LINUX SHELL
### By Filipe Chagas

A small Linux command interpreter implemented using the kernel syscall interface. It was done for a college exam that has already happened.

## Syntax 
* No arguments:	[command]
* Single argument:	[command] [arg]
* Two arguments:	[command] [arg_0] [arg_1]
* _N_ arguments:	[command] [arg_0] [arg_1] ... [arg_{N-1}]

## Available commands

| Command | Arguments | Description | Usage Example |
|---------|-----------|-------------|---------|
| **help**    |           | Print informations about the shell. | help |
| **pwd**     |           | Print current working directory path. | pwd |
| **cd**      | destination_path  | Change working directory path. | cd /home |
| **ls**      | path _(optional)_ | Lists entries in the directory (argument directory or working directory). | ls |
| **exec** | path, \[arg\_1 , ... , arg\_n\] _(optional)_| Execute the _path_ file. | exec echo hello |
| **exit**    |           | Close the shell. | exit |


