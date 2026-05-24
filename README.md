# Orbital Stike Malloc ☄️

This program purpose is to check for any improper malloc handling by replacing the real malloc with the custom malloc. 
After that, you can set behavior of malloc as you wish.

### Behavior setting option

In the `malloc_strike.c` you can change this setting to set behavior of malloc.
```
# define	MAX_MALLOC_CALLS	10000		// maximum number of malloc calls
# define	MAX_MALLOC_BYTES	1000000		// maximum number of bytes allocated (1MB default)
# define	MALLOC_ID_FAIL		-1UL		// forces the malloc of that ID to fail (-1UL to unset).
# define	PRINT_WARNINGS		true		// enable warnings (not necessary a fail)
# define	PRINT_CALLS			true		// print all malloc calls
```
## Quick start

### Opiton 1: Create your own malloc_strike file

You can create you malloc_stike.c file and put the source code into the file and compile it with target file.

### Option 2: Git clone option

Run this command below in your root repository and it will clone the malloc_strike file into your root repository.

```
git clone git@github.com:kaituitei/malloc_strike.git && cd malloc_strike
mv malloc_strike.c ..
cd ..
rm -rf malloc_strike
```

### Repository structure

```
.
├── malloc_strike.c
└── test.c
```

### Usage

Compile `malloc_strike.c`  with you target program

Ex.

```cc -Wall -Werror -Wextra your_program.c malloc_strike.c```

<sub><sub>*Replace `your_program.c` to your file target name.</sub></sub>

### Example
Normal situation - Not limit size of malloc

