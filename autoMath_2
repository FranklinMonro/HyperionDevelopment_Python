f = open('input_optional.txt', 'r+')#open file
for lines in f.readlines():#for loop to read through txt file
    data = lines[0:4]#splice txt file from 0 to 3
    data2 = lines[5:]#splice txt file index 4 to end
    data3 = data2.split(',')#split at ,
    data4 = [int(i) for i in data3]  #cast string to integer in data 3
    if data == "min:":#if statement when data is equal to min
        print("The min of " + data2.strip('\n') + " is: " + str(min(data4)))
    elif data == "max:":#if statement when data is equal to max
        print("The max of " + data2.strip('\n') + " is: " + str(max(data4)))
    elif data == "avg:":#if statement when data is equal to avg
        print("The avg of " + data2.strip('\n') + " is: " + str(sum(data4)/len(data4)))
    elif data == "sum:":#if statement when data is equal to sum
        print("The sum of " + data2.strip('\n') + " is: " + str(sum(data4)))
    elif data == "p90:":#if statement when data is equal to p90
        print("The 90th percentile of " + data2.strip('\n') + " is: " + str(round(0.9*len(data4))))
    elif data == "p70:":#if statement when data is equal to p70
        print("The 70th percentile of " + data2.strip('\n') + " is " + str(round(0.7*len(data4))))
    else:
        print("There is no other operation")

  
        
f.close()#close file
