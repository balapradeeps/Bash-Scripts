#### The read command is used to accept input from the user and assign it to a variable. The -p option is used to specify a prompt to display to the user before accepting input.
```
#!/bin/bash

# accept input variables
read -p "Enter variable 1: " var1
read -p "Enter variable 2: " var2
read -p "Enter variable 3: " var3

# print out the input variables
echo "Variable 1: $var1"
echo "Variable 2: $var2"
echo "Variable 3: $var3"
```
```
We can pass the arguments one by one 
- > Run Command : sh var.sh
Enter variable 1: loki  //var1 input
Enter variable 2: thor  //var2 input
Enter variable 3: odin  //var3 input
```

#### Alternatively, we can also use command-line arguments to pass variables to the script like below:
```
#!/bin/bash

# assign input variables to command-line arguments
var1=$1
var2=$2
var3=$3

# print out the input variables
echo "Variable 1: $var1"
echo "Variable 2: $var2"
echo "Variable 3: $var3"
````

```
In this case, we can pass the variables to the script when you run it, like this:
- > Run Command : sh var.sh value1 value2 value3
```

#### We can also use shift command to get multiple arguments in a while loop.

```
#!/bin/bash

while [ $# -gt 0 ]; do
    echo "argument: $1"
    shift
done
````
```
We can pass the arguments while running the script.
- > Run Command : sh var.sh loki thor odin hela valkari 
```
