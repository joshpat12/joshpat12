-Module 4 Project
Course 40461: Introduction to Python, Unit 2

This is an activity based on the Module 4 Lab, which you may have already completed.

Assignment Requirements
NOTE: This program requires print output and code syntax used in Module 4 such as variable assignment, input, while, open keywords, .split(), .readline(), .seek(), .write(), .close() methods.
The Weather
Create a program that:
Imports and opens a file
Appends additional data to a file
Reads from the file to displays each city name and month average high temperature in Celsius
Output: The output should resemble the following

City of Beijing month ave: highest high is 30.9 Celsius
City of Cairo month ave: highest high is 34.7 Celsius
City of London month ave: highest high is 23.5 Celsius
City of Nairobi month ave: highest high is 26.3 Celsius
City of New York City month ave: highest high is 28.9 Celsius
City of Sydney month ave: highest high is 26.5 Celsius
City of Tokyo month ave: highest high is 30.8 Celsius
City of Rio De Janeiro month ave: highest high is 30.0 Celsius
All of the above text output is generated from the file. Only these strings are hard coded:

"is"
"of"
"Celsius"
Import the file into the Jupyter Notebook environment
Use !curl to download https://raw.githubusercontent.com/MicrosoftLearning/intropython/master/world_temp_mean.csv as mean_temp.txt
# [ ] The Weather: import world_mean_team.csv as mean_temp.txt into the Jupyter notebook

Add the weather for Rio
Open the file in append plus mode ('a+')
Write a new line for Rio de Janeiro "\nRio de Janeiro,Brazil,30.0,18.0"
Grab the column headings
Use .seek() to move the pointer to the beginning of the file
Read the first line of text into a variable called: headings
Convert headings to a list using .split(',') which splits on each comma
# [ ] The Weather: open file, read/print first line, convert line to list (splitting on comma)
- 
-  
-    mean_temp = open('mean_temp.txt', 'r')
read_line = mean_temp.readline()
print(read_line)
heading = read_line.split(',')
print('Heading list: ',heading)
city_temp = ''
while read_line:
    print(read_line[:-1]) # writes the first line in the file
    read_line = mean_temp.readline() # goes to the next line
    city_temp += read_line  # adding the line to the variable
    city_temp1 = city_temp.split(',') # split the line every comma to a list

print(city_temp1)
