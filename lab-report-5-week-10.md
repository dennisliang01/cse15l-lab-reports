# Week 10 Lab Report 5
March 9th 2022

Last Updated: March 9th, 2022 by Dennis Liang

# Different Answers from Differnt Implementation

## How I Found the Tests With different Reuslts

To find the different tests with different results took me several steps.
First I ran the bash script for my implementation of the markdown parse
and the professor's version of the markdown parse. I stored each of the bash 
script output in a text file called results.txt. Then I used diff to compare
the results of the two results.txt file. I stored  the results of the diff
commmand in a file called compareResults.txt and it showed me all the
tests where there were differnt results.

## Tests With Different Results

## Test 1
### Test File: 201.md
```
[foo]: <bar>(baz)

[foo]
```

Expected Result:

![Image](lab-report-5-images\Screenshot 2022-03-11 152205.png)

```
[]
```

### Actual Output ("<" = Mine, ">" = Professor)
![Image](lab-report-5-images\Screenshot 2022-03-11 151819.png)

According to the commonmark demo website, my implementation is correct because
the given file does not contain any valid link. Therefore, the markdownparse
program should not have stored anything in the output list.

The bug is that the professor's markdown parse is ignoring the "<>". In
markdown, the "<>" is often used to indicate formatting such as bold or italicize. 
To fix this issue, the best thing to do is to add a statement to check if there
are any "<" or ">" in the each line. This could be inserted after line 64
below. The program would then skip until there is an equivlaent "</>"
character and restart looking for open square brackets. 

![Image](lab-report-5-images\Screenshot 2022-03-11 154520.png)

## Test 2

### Test File: 487.md
```
[link](/my uri)
```

Expected Result:

![Image](lab-report-5-images\Screenshot 2022-03-11 164103.png)

```
[]
```

### Actual Output ("<" = Mine, ">" = Professor)
![Image](lab-report-5-images\Screenshot 2022-03-11 163900.png)

According to the commonmark demo website, my implementaion of the markdown parse
program is wrong for the given test. The actual output should be no link
added to the list. However, my output added a link to the list. The professor's
output is correct and did not include anything to the output.

My version of the markdown parse program is not detecting spaces in the ().
Having spaces would make any text within the () not a link. I would need 
to add a way to detect if there are spaces within the link. To do this,
I can simply check before line 24 that if the string to be added to the list
contains any spaces. If the string contains any spaces, I simply don't add
the string to the list of links.

![Image](lab-report-5-images\Screenshot 2022-03-11 164531.png)