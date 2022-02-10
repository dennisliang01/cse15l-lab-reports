# Week 6 Lab Report 3
February 11th 2022

Last Updated: February 10th, 2022 by Dennis Liang

## Streamling ssh Configuration
### .ssh/config file
![Image](lab-report-3-images\Screenshot 2022-02-10 142740.png)

Here I took the example from the lab page and added my own user name. Other than that I left the other options set to the default setting.

### ssh Command Using Alias
![Image](lab-report-3-images\Screenshot 2022-02-10 143108.png)

Here I logged into the remote server using my alias "ieng6". This step was simple and quick I simply typed "ssh ieng6". Using an alias is much quicker than typing out my username and my password. This also makes future local to remote server actions faster.

### scp Command Using Alias
![Image](lab-report-3-images\Screenshot 2022-02-10 152643.png)

Initially I had trouble using the alias to copy files to the server. My computer treated the alias as a new file name. I solved this problem by specifying where within ieng6 I want my file to be pasted.
