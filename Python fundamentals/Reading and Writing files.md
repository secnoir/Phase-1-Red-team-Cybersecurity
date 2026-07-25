Python can be used to read files and also write to files.When we want to perform read and write in python we typically have 3 modes which we can use. read(r) , Write(w) , Append(a). When we use write(w) it removes the existing information in the file , so if we want to keep the file as it is and add something to it we can use append(a).

Example:

Suppose we have a text file called football.txt , inside that file we have :

Messi

Ronaldo

Neymar

Mbappe

Bellingham

Yamal

We are going to append another footballer's name to this file and then read it.


with open("football.txt", "a") as file:

     file.write("\nMaradona")

with open("football.txt", "r") as file:

    print(file.read()) 

Output: 

Messi

Ronaldo

Neymar

Mbappe

Bellingham

Yamal

Maradona

