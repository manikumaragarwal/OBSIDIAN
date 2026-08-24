

--09-03-2026 22:27

Tags: [[CODING]]

---
# BASH SCRIPTING

- **SHABANG** - used to tell the shell that it's written in BASH 
```BASH
#! /bin/bash
```


---
- making a file **Executable**
```bash
chmod +x filename.sh
```


---
- Normal Variables declaration (**no spaces**)
```BASH
name="inputvalue"

echo "this is your $name"
```


---
- taking **Input** as an variable
```bash
echo "enter the variable as input"

# this is how we take input : "read"
read input 

# it's important to declare a varaible before taking the input
echo "this is my $input"
```


---
- **Positional parameter** : giving the input, in the same command as executing the file.sh
```bash

# $1 means, variable having 1st position
variable1=$1
variable2=$2


echo "this is $variable1"
echo "this is $variable2"

```

```shell
# while executing the file : 

./filename.sh firstvariable secondvariable
```

---

## References-
https://www.youtube.com/watch?v=7qd5sqazD7k