# 

ooo boi functions this next part is a mind fuck

***odd even example***




def exists(ls, elem):
    i = 0
    while len(ls) > i:
        if ls[i] == elem:
            return True
        i += 1
    return False

# put your testing code down here
names = ['Lelouch', 'Karen', 'Zero', 'Suzaku']

print(exists(names, 'Karen'))   # should print: True
print(exists(names, 'Suzaku'))  # should print: True
print(exists(names, 'Pikachu')) # should print: False
print(exists(names, 123))       # should print: False