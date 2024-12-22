# wc-tool-ocean
This script is to build my own version of the Unix command line tool wc!

## The functional requirements for wc are concisely described by it’s man page - give it a go in our local terminal now:

```
man wc
```

### Step Zero
Like all good software engineering we’re zero indexed! In this step we’re going to set our environment up ready to begin developing and testing our solution.

We'll setup our IDE / editor of choice and programming language of choice. After that here’s what I’d like us to do to be ready to test our solution.

We already have test.txt file in this repository.

### Step One
In this step our goal is to write a simple version of wc, let’s call it ccwc (cc for Coding Challenges) that takes the command line option -c and outputs the number of bytes in a file.

If we’ve done it right our output should match this:


```
>ccwc -c test.txt
  342190 test.txt
```

If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! On to…

### Step Two
In this step our goal is to support the command line option -l that outputs the number of lines in a file.

If we’ve done it right our output should match this:

```
>ccwc -l test.txt
    7145 test.txt
```
If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! On to…

### Step Three
In this step our goal is to support the command line option -w that outputs the number of words in a file. If we’ve done it right our output should match this:

```
>ccwc -w test.txt
   58164 test.txt
```
If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! On to…

### Step Four
In this step our goal is to support the command line option -m that outputs the number of characters in a file. If the current locale does not support multibyte characters this will match the -c option.

we can learn more about programming for locales here

For this one our answer will depend on our locale, so if can, use wc itself and compare the output to our solution:

```
>wc -m test.txt
  339292 test.txt

>ccwc -m test.txt
  339292 test.txt
```
If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! On to…

### Step Five
In this step our goal is to support the default option - i.e. no options are provided, which is the equivalent to the -c, -l and -w options. If we’ve done it right our output should match this:

```
>ccwc test.txt
    7145   58164  342190 test.txt
```
If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! On to…

### The Final Step
In this step our goal is to support being able to read from standard input if no filename is specified. If we’ve done it right our output should match this:

```
>cat test.txt | ccwc -l
    7145
```
If it doesn’t, check our code, fix any bugs and try again. If it does, congratulations! we’ve done it, pat ourself on the back, job well done!

