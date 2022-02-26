# Week 8 Lab Report 4
February 25th 2022

Last Updated: February 25th, 2022 by Dennis Liang

## Repositories
[Personal](https://github.com/dennisliang01/markdown-parse)

[Other Group](https://github.com/codyprupp/markdown-parse)

## Expected Output For Each Snippet
Based on outputs from this webesite [here](https://spec.commonmark.org/dingus/)

### Snippet 1

```
[`google.com, google.com, ucsd.edu]
```
![Image](lab-report-4-images\Screenshot 2022-02-25 152221.png)

### Snippet 2

```
[a.com, a.com(()), example.com]
```
![Image](lab-report-4-images\Screenshot 2022-02-25 152536.png)

### Snippet 3

```
[https://ucsd-cse15l-w22.github.io/]
```
![Image](lab-report-4-images\Screenshot 2022-02-25 152811.png)


## Personal Markdown-Parse Repository
Link to personal repository [here](https://github.com/dennisliang01/markdown-parse)

### Snippet 1
![Image](lab-report-4-images\Screenshot 2022-02-25 155553.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 155634.png)

Did not pass the test

### Snippet 2

![Image](lab-report-4-images\Screenshot 2022-02-25 155754.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 155933.png)

Did not pass the test

### Snippet 3

![Image](lab-report-4-images\Screenshot 2022-02-25 160149.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 160214.png)

Did not pass the test

## Other Group Markdown-Parse Repository
Link to personal repository [here](https://github.com/codyprupp/markdown-parse)

### Snippet 1

![Image](lab-report-4-images\Screenshot 2022-02-25 162600.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 162628.png)

Did not pass the test

### Snippet 2

![Image](lab-report-4-images\Screenshot 2022-02-25 162700.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 162719.png)

Did not pass the test

### Snippet 3

![Image](lab-report-4-images\Screenshot 2022-02-25 162741.png)
![Image](lab-report-4-images\Screenshot 2022-02-25 162814.png)

Did not pass the test

## Answers to Questions

Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

- I definetly think that I can implement a change to detect the back tick. I simply
have to detect the open back tick and close back tick and ignore everything in between.

Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

- To handle the parentheses and bracket cases I would need to implement a stack data structure
to keep track of the open and close parentheses and brackets. This way I know how does the
nested parenthese and brackets interact with each other. However, this would probably take
longer than 10 lines.

Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

- I think to handle the new lines within bracekts and parentheses I would need to detect
if the current index is at the end of the file string. If there is a close bracket or parentheses
I would just ignore them. This should be less than tne lines.