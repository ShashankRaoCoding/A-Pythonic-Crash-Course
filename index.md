Before starting this tutorial, it would help if you have python installed. However, you can use the python interface on [this website]() that runs python code for you in the browser. 

# Assigning Variables 
You can think of variables like boxes. You can store something in a variable, and you can store variables in other variables. It'll make more sense once you look at the code. Variables can be names anything you like. I've named mine bartholomew: 
```bartholomew = 5```
The above line of code assigns the value of '5' to a variable names 'bartholomew.' Now, this may sound simple enough at first, but something strange is actually going on behind the screen. Take a look at this code: 
```
x = 5 
y = x 
x = 10 
```
Looking at the above code, what do you think the value of y is when you read line 3? If you said 10, you'd be (understandably) upset to find out that the answer is 5. 

Strange? Well the issue does not lie with the understanding of how variables work, but instead in understanding how the '=' sign works. Here is how you *should* be thinking of any assignment statement: 

When you say `[some variable name] = [some value]`, what Python does is first look at `[some value]` as a mathematical expression to be evaluated. For example, if I said "evaluate 5+5" you'd say (hopefully) "10". Now how about I say "evaluate 5"? Since you're not doing anything to the 5, you get the value 5 from evaluating it. Python evaluates the expression to the right of the '=' and then stores the *result* in the variable, but **does not store the expression itself**. Looking back at the code example, let's rewrite it a bit to show what the computer is thinking (lines with `#` are ignored by computer - these are called comments). 

```
x = 5 
# computer evaluates '5' to result in '5' and stores this '5' in 'x' 
y = x 
# computer evaluates 'x' to result in '5' and stores this '5' in 'y' 
x = 10 
# computer evaluates '10' to result in '10' and stores this '10' in 'x' 
```

Notice how the value of `y` does not change, despite it being defined as the value of `x`. This may seem trivial to begin with, but in a few chapters this trivial concept forms the lynchpin of various algorithmic possibilities. 

But just using numbers isn't particularly exciting, so let's expand! 
``` 
# this is a string - a collection of ordered alphanumeric characters 
bartholomew = "hi" 
# computer evaluates "hi" to result in "hi" and stores this in 'bartholomew'
```

Surrounding any collection of alphanumeric characters in quotation marks makes them a string, such as "hi", "hello", "or even this text, yes you can store more than one word." 

Quick question! Are `x = 5` and `y = "5"` the same? Since I'm asking, you probably realise that the answer is no. And you'd be right, *5* is an integer, but *"5"* is string - a collection of one character (the character '5'). 

> [!Key Term: Algorithm ]
> An algorithm is a set of steps. For example, "go straight, then take a right, and then the second left" is an algorithm to... I'm not sure where but you get the idea. 
# The print Statement and some tricks 
So far we've stored a value in a variable, but if you run the code you'll notice that nothing is outputted. This is because we haven't told python to output anything! 

A simple function to do this is called the 'print' function. But before we get to that, let's take a look at what functions are! 

## How to think about functions programmatically 
A function is a machine. You give it some raw materials, it processes them, and then produces a product. The manner in which it processes them is always the same, even if you give it varying raw materials. Like a washing machine, for example! it doesn't matter what clothes you put in it, their colour or size, they are returned in a cleaner state (hopefully) than when you put them in. Notice that the output still depends on the input, even if the steps are the same. **Most importantly**, if you give the same inputs, you *always* get the same output. 

---

In Python, a function is a machine, and the raw materials it takes are called *arguments*. For example, the *print* function takes a *string* and outputs it to the *console* (the giant black space to the right). The writing is identical to mathematical notation. For example, 
$$
f(x) = x + 5 
$$
would mean that 
$$
f(5) = 5 + 5 = 10 
$$

Similarly, 
`print("hi")`

Would produce an output, namely, the displaying of the string "hi" in the *console*. Run it and see! 

> [!Bonus: ] 
> Now try print(5)! Do you get an output? Yes? Strange? After all, didn't I say 5 is an integer, and not a string? Well, the print function automatically converts it! Pretty nifty! 

# Mathematical Operators 
Now we get to some actual processing! First off, the basic mathematical operators remain the same: 
```
x = 5 
y = 10 
z = x + y 
print(z) 
# output should be 15 
```

You can also simply say `print(5 + 10)` or `print(x + y)`and get the same result. The way python handles this is to first evaluate the *arguments* as a mathematical expression, then feed the result into the function. 

Subtraction is the simple `-` sign, but division is divided into 2 forms! 

## Division 
`//` vs `/` 
Evaluating `x = 11/2` results in `x = 5.5`
Evaluating `x = 11//2` results in `x = 5` 

Caught on yet? When you use `//`, any remainder is ignored. When you use `/`, it is evaluated like normal division. 

But hey! What *is* `5.5`? It's not an integer, since it has a decimal value, but it's not a string either? 

Decimal values are stored in a third form of data, called ***floats***. You can treat them just as you would regular decimal numbers, for now. 

## Multiplication and Powers 
Multiplication uses the conventional `*`, but putting `**` means *raised to the power of.* 
For example `2*5` evaluates to `10` but `2**5` evaluates to `32`. 

> [!Question: ] 
> What do you think happens when a string is added to a string? For example: 
> ``` 
> bartholomew = "hi" + "sup" 
> print(bartholomew) 
> ```
> The output is "hisup"! Now what about: 
> ```
> bartholomew = "hi" + 5 
> print(bartholomew) 
> ```
> The output is... an error message. Python does not allow you to add different types of data to each other (except for floats and integers). 

# Basic Data Structures 

# Loops 
