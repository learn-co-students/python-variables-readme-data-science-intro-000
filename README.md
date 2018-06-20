
# Naming things with Variables

### Introduction

> "There are only two hard things in Computer Science: cache invalidation and naming things."

> -- Phil Karlton

> "...But ordinary language is all right."

> Ludwig Wittgenstein

### Objectives

* Learn about how to use variables to give meaning to data
* Learn how to assign a variable to data
* Learn how to declare a variable
* Learn how to reassign a variable

### Declaring and Assigning Variables

So far we have worked with data -- strings, numbers, and booleans.  In this lesson, we'll learn how to use variables to assign names to this data.  For example, this is a string from our Working with **Data Types Lab**.


```python
"art vandelay"
```




    'art vandelay'



Now months later, if we see that string in some code, we may be confused as to what it is, and with even more data, this only becomes more difficult. Think of what we saw in our **Data Types Lab**: `"art.vandelay@vandelay.co"`, `"Ceo"`, `"7285553334"`, `"vandelay.com"`. There's a lot to keep track of.

So, let's use variables to indicate what each of these strings mean.


```python
email = "art.vandelay@vandelay.co"
```

> **Note:** For this, and all of the subsequent code in gray boxes, you should press shift + enter to ensure that the code executes. If you do not do so with the line above for example, then when we reference `email` in the lines that follow, Jupyter will throw an error indicating that the variable is undefined. So, it is not enough to just type the correct code, we need to run shift + enter on our gray boxes to run this code.

In programming terms, we say that we just declared a variable, `email`, and assigned it to the string, `"art.vandelay@vandelay.co"`.  To do so, we'll follow the procedure below:

    variable = data

Now that we have assigned a variable `email` to a string, we just type the word `email` to see the string again.


```python
email
```

> *remember to press shift + enter on the gray box above to see the value of our variable, *`email`*.*

Now let's try this with the website:


```python
website = "vandelay.com"
website
```

Note that if you introduce a new variable, (declare it), but do not also assign it in the same line, Python will raise an error.


```python
name
```


    ----------------------------------------------------------

    NameError                Traceback (most recent call last)

    <ipython-input-6-9bc0cb2ed6de> in <module>()
    ----> 1 name


    NameError: name 'name' is not defined


So that error tells us that `name` is not defined.  We just fix this by declaring `name` and assigning the variable in the same line.


```python
name = 'Art Vandelay'
name
```

So this is assigning and reading a variable.  And when we want to see some information again, we can easily find out.


```python
email
```

### Declaring variables without assignment

We have seen that we can have data without assigning it to variables.  


```python
"Unassigned data"
```




    'Unassigned data'



Sometimes we wish to declare a variable without assigning it to data.  In Python, that's a little tricky to do.  As we just saw with `name`, declaring variables without assignment throws an error.  Thankfully, Python has a special type for us that represents nothing at all.


```python
None
```


```python
type(None)
```




    NoneType



None is a data type in Python that represents nothing.  So, if we do not know the type of a variable and want to have the data to the variable be assigned later, we can assign that variable to `None`.


```python
address = None
```

Notice that `address` is now assigned, but it is assigned to `None`.


```python
address
```

**Note:** *when variables are assigned to `None`, pressing shift + enter on the cell block will not output anything.*

### Reassigning variables

Now that we have this data, we can imagine using it for some kind of instruction.  For example, say we want to write ourself a memo on how to reach out to someone we just met. Here's the message:


```python
"Send an email to Art Vandelay at 'art.vandelay@vandelay.com' to say how nice it was meeting yesterday."
```

If we construct this message with variables, we can write the following:


```python
name = "Art Vandelay"
email = "art.vandelay@vandelay.com"
```


```python
"Send an email to " + name + " at " + email +  " to say how nice it was meeting yesterday."
```

Now you meet someone else, "Liz Kaplan" with the email of "liz@ka-plan.com" and want to write a memo with the same instructions, but the only thing that varies are the name and email. This should be easy enough given the way we set up our memo above. First we need to change the variables, `name` and `email`, by setting them to our new data.


```python
name = 'Liz Kaplan'
email = 'liz@ka-plan.com'
```

So as you can see, we reassign our variables by just setting `variable = 'new data'`. Presto, our variable is then updated.


```python
name # 'Liz Kaplan'
```


```python
email # 'liz@ka-plan.com'
```

Now, if we copy and re-run our previous code, we will see it is automatically updated.


```python
"Send an email to " + name + " at " + email +  " to say how nice it was meeting yesterday."
```

So in the line above, we are getting to some of the real power of programming.  By choosing the correct variable name, we can begin to change the values of `name` or `email` and operate on their underlying values in the same ways.

### Operating on variables

Just to hammer this point home let's see what we can now do with the name variable.


```python
name
```


```python
name.upper()
```


```python
name.title()
```

Just like how we are able to directly call methods on a string, we can also call methods on a variable that points to a string.  And, if we try to call a method on something that we think is a string, but really is a number, we will see an error.


```python
name = 42
```


```python
name.upper()
```

We receive the same error from calling `upper` directly on the number `42` as we do when we call `upper` on a variable that points to the number `42`. So, now that we are working with variables, we may run into errors where we thought a variable is one thing, but it is actually something else. Don't worry, this is no big deal.  We can just check to see what the variable is.


```python
name
```

Once we have see what the variable is, we can make our change.


```python
name = 'Liz Kaplan'
name
```

### Summary

In this lesson, we got a taste for what makes computer programs so powerful.  By using variables, we can write programs that know how to combine data.  This can save us time by avoiding boring, repetitive tasks.  We declare and assign a variable with the pattern of `variable = data`, and reassign a variable with the same pattern.  To reference a variable, we simply type the variable's name.  

We also saw that one of the things to pay attention to when working with variables is that they are sometimes different from what we expect.  So we just type the name of the variable, to see what it really is and make any necessary changes.
