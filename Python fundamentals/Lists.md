Lists are a collection of multiple items stored in a single variable.

Example :

phones = ["Iphone" , "Samsung" , "Xiaomi" , "Redmi"]

Lists are mutable meaning we can change them.

phones.append("Nokia") #Adds Nokia at the end of the list.

phones.insert(2, "Huawei") #Inserts Huawei at index 2 in the list.

phones.remove("Redmi") #Removes Redmi from the list.

phones.pop(1) #Removes the item at index number 1.


We can also add two lists together.

Suppose we have two lists phones and smartphones and we want to add them we can do :

all_phones = phones + smartphones

We also have nested lists , which means a list inside another list. They look something like :

iq_scores = [["Bob", 92] , ["Alice",112] , ["John" , 110] ]  #Nested list

alice_iq = iq_scores[1]  [1]  #Takes the number 1 index from parent index number 1

print(alice_iq)

OUTPUT :

112


We can change items in nested lists too.

iq_scores[0]  [1] = 97   #Changes Bob's iq score to 97




