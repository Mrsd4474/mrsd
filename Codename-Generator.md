The following code is for internal or external use.
It generates slur and cuss safe English words for new build code names.

```Python
# Austin H
# CodeName Generator
start_version_code_name = 49
english_letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
english_vowels = ['a','e','i','o','u','y']
english_constants = ['b','c','d','f','g','h','j','k','l','m','n','p','q','r','s','t','v','w','x','z']
size_english_alphabet = len(english_vowels)+len(english_constants)
cool_pairs = [('i','ngus'), ('e','tut'), ('e','mus'), ('o','kip'), ('i','ngo'), ('i','nymo'), ('i','git'), ('u','nky'), ('y','tot'), ('e','ham'), ('a','bub'), ('i','yun'), ('a','mut'), ('o','tut'), ('i','tag'), ('i','mon')]
# when codenames run out please new ones to cool_pairs
f = open("code_name.lst","w")

if (26 != size_english_alphabet): # sanity check
    print("alphabet wrong")
else:
    if (26 != len(english_letters)): # sanity check
        print("alphabet wrong")
    else:    
        for pair in cool_pairs:
            mid, suffix = pair
            for letter in english_letters: # loop through english alphabet
                if letter in english_vowels:
                    f.write(str(start_version_code_name) + " " + letter + suffix + "\n")
                else:
                    f.write(str(start_version_code_name) + " " + letter + mid + suffix + "\n")
                start_version_code_name = start_version_code_name + 1

f.close()
```
