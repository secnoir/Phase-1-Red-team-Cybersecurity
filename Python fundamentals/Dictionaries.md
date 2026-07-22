A dictionary is a collection of data stored in key value pairs.Dictionaries use curly brackets {} . They are mutable , stores data using keys and values.
Example : 
student = {
     "name": "irfan",
     "age": 18
}
print(student["name"])

Lets say we want to add a new key/value pair.We can add simply by :
student["course"] = "python"

If we only want to change a value we can do :
student["age"] = 19

now if we print student we get output :
student = {
     "name": "irfan",
     "age": 19,
     "course": "python"
}