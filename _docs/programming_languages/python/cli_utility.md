---
layout: default
title: Command-line Utility
parent: Python
grand_parent: Programming Languages
---

# Command-line Utility

## Create a command-line application
Template for creating an application that takes arguments and does something with it (requires the `sys` module only):

```python
from sys import argv, exit


def usage():
    """This is a help page
    """

    print("""example.py [OPTIONS]

This template demonstrates a command-line utility script.

Example: parser.py --value --help

Options:
        --hello [value]                             call a hello function

Values:
        --world                                     the world argument
""", end='')

    exit(0)


def validate_arg(argv: list, arg_vars: dict, arg: str):
    """Validates a given argument's value

    With a given argument 'arg', validates that it is a valid key
    in 'arg_vars'. Also validates the argument's value based on what comes
    after it in the list 'argv'.

    Parameters:
        - argv (list): the command-line arguments given by the user
        - argv_vars (dict): list of valid arguments
        - arg (str): argument to validate
    """

    if (i + 1 < len(argv)):
        if (argv[i + 1] in arg_vars.keys()):
            print('Missing argument:', arg)
            exit(2)
    else:
        print(f'Missing argument: {arg}')
        exit(2)


def hello(arg_vars: dict):
    """This is an example function called by the user
    """

    print(f'Hello, {arg_vars['--name']}!')


# list of functions that arguments can call
arg_funcs = {
    '--hello': hello,
}

# list of variables that an argument may take and can be used in functions
arg_vars = {
    '--name': '',
}

# we create a hard copy of argv to avoid manipulating it,
# then we remove the file name from the new array
process_argv = argv.copy(); process_argv.pop(0)

# call the help page
if process_argv[0] == '-h' or process_argv[0] == '--help':
    usage()
    exit(0)

skip_arg = False                            # whether to skip the next argument

# iterate all argv for the first found argument for function call
for key in arg_funcs.keys():
    for arg in process_argv:
        if key == arg:
            execute_function = arg_funcs[f'{key}']
    if skip_arg == True:                    # exit loop if the function was found
        break

for key in arg_vars.keys():
    for i, arg in enumerate(process_argv):
        if skip_arg:
            skip_arg = False
            continue

        if key == arg:
            validate_arg(process_argv, arg_vars, key)
            arg_vars[f'{arg}'] = process_argv[i + 1]
            skip_arg = True

try:
    execute_function(arg_vars)
except NameError e:
    print(e)
    print(f'{argv[0]}: Could not execute the command')
```

To create a new command, add an argument for it in the `arg_funcs` dictionary and the function as its value. (**NOTE**: the value as function should only include the function name). Then, create a new function and add the dictionary `arg_vars` as its parameter. You now have access to the full list of the user's arguments and their values.

Example:
```python
def foo(arg_vars: dict):
    print(f'{arg_vars['--bar']}')

arg_func = {
    '--foo': foo,
}

arg_var = {
    '--bar': '',
}
```
