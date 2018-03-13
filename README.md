
# Naming things with Variables

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

So far we have only worked with data.  Strings, numbers, True and False.  In this lesson, we lesson we learn how to use variables to assign names to this data.  For example, this is a string from our Working with Data Types Lab.


```python
"art vandelay"
```




    'art vandelay'



Now months later, if we see that string in some code, we may be confused as to what it's about.  And when we add more data, this only becomes more difficult.  Think of the what we saw in our Data Types Lab: `"art.vandelay@vandelay.co"`, `"Ceo"`, `"7285553334"`, `"vandelay.com"`.  There's a lot to keep track of.

So let's use a variables to indicate what each of these strings mean.


```python
email = "art.vandelay@vandelay.co"
```

In programming terms, we say that just "declared a variable `email` and assigned it to the string `"art.vandelay@vandelay.co"`".  And to do so, we'll follow the procedure above:

`variable = data`

Now that we have assigned a variable `email` to a string, we just type the word `email` to see the string again. 


```python
email
```




    'art.vandelay@vandelay.co'



Ok, let's do this with the website too.


```python
website = "vandelay.com"
website
```




    'vandelay.com'



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
name = 'Art Vandalay'
name
```




    'Art Vandalay'



So this is assigning and reading a variable.  And when we want to see some information again, we can easily find out.


```python
email
```




    'art.vandelay@vandelay.co'



### Reassigning variables

Now that we have this data, you can imagine using it for some instructions.  For example, say you want to write yourself - if you're fortunate, a direct report - some instructions on who and how to reach out to someone you just met.  Here's the message:


```python
"Send an email to Art Vandalay at 'art.vandelay@vandelay.com' to tell say how nice it was meeting yesterday."
```




    "Send an email to Art Vandalay at 'art.vandelay@vandelay.com' to tell say how nice it was meeting yesterday."



If we construct this message with variables, we have the following:


```python
"Send an email to " + name + " at " + email +  " to say how nice it was meeting yesterday."
```




    'Send an email to Art Vandalay at art.vandelay@vandelay.co to say how nice it was meeting yesterday.'



Now, you meet someone else, "Liz Kaplan" with the email of "liz@ka-plan.com" and want to give the same instructions, but the only thing that varies are the name and email.  So then this is easy enough.  First we change what the data that the variable points to.


```python
name = 'Liz Kaplan'
email = 'liz@ka-plan.com'
```

So as you can see, we reassign our variable by just setting `variable = 'new data'`.  And our variable is then updated.


```python
name # 'Liz Kaplan'
```




    'Liz Kaplan'




```python
email # 'liz@ka-plan.com'
```




    'liz@ka-plan.com'



And now, our previous message is automatically updated.


```python
"Send an email to " + name + " at " + email +  " to tell him how nice it was meeting him yesterday."
```




    'Send an email to Liz Kaplan at liz@ka-plan.com to tell him how nice it was meeting him yesterday.'



So in the line above, we are getting to some of the real power of programming.  By choosing the correct variable name, we can begin to say treat this data like a `name` or an `email`, regardless of what the underlying value is.  And then we can perform easily perform the same operation on different underlying values. 

### Operating on variables

Just to hammer this point home let's see what we can now do with the name variable.


```python
name
```




    'Liz Kaplan'




```python
name.upper()
```




    'LIZ KAPLAN'




```python
name.title()
```




    'Liz Kaplan'



So just like we directly call methods on a string, we can also call methods on a variable that points to a string.  And, if try to call a methods on something that you think is a string, but really is a number, you will see an error. 


```python
name = 42
```


```python
name.upper()
```


    ----------------------------------------------------------

    AttributeError           Traceback (most recent call last)

    <ipython-input-19-ef33b7f2c4e1> in <module>()
    ----> 1 name.upper()
    

    AttributeError: 'int' object has no attribute 'upper'


Just like we would recieve that error from calling on number `42` more easily.  So now, that we are working with variables, you may run into errors where you think a variable is one thing, but really it is something else.  But it's no big deal.  We just see what the variable is.


```python
name
```




    42



And make the change.


```python
name = 'Liz Kaplan'
name
```




    'Liz Kaplan'



### Summary

In this lesson, we got a taste for what makes computer programs so powerful.  By using variables, we can write programs that know how to combine data.  This can save us time by avoiding boring, repetitive tasks.  We declare and assign a variable with the pattern of `variable = data`.  And reassign a variable with the same pattern.  To refernece a variable, we simply type the variable's name.  

We also saw that one of the things to pay attention to when working with variables is that they are sometimes different from what we expect.  So we just type the name of the variable, to see what it really is and make the change. 
