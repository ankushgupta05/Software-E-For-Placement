Aap kehna chahte ho:

Capture: Yaha par customer ka naam store hota hai.

Weep: Yeh ek dictionary (dict) type ka data structure hai jisme Customer aur Supplier dono ka data store kiya ja sakta hai.


👉 Matlab simple shabdon mein:

Customer aur Supplier dono ko ek dictionary ke form mein rakhoge.

Dictionary ka structure aisa ho sakta hai:


data = {
    "Customer": {
        "name": "Ankush",
        "address": "Bhopal",
        "phone": "9876543210"
    },
    "Supplier": {
        "name": "Rahul",
        "address": "Indore",
        "phone": "9123456780"
    }
}

Ab agar customer ka naam capture karna ho, to:

print(data["Customer"]["name"])  
# Output: Ankush

Aur agar supplier ka naam chahiye, to:

print(data["Supplier"]["name"])  
# Output: Rahul


---

Kya aap chahte ho mai aapko ek poora dictionary structure bana kar dikhau jo Customer aur Supplier dono ke multiple records store kar sake?

