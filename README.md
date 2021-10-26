- mean_temp = open('mean_temp.txt', 'r')
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
