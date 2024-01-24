
import bcrypt

hashed_keys = []

def main():
    while True:
        input_key = input("Enter keys for assignment (if you have finished enter 'END')")
        if input_key == 'END': # End of the request *Key sensitive
            break
        # Password restrictions for being safe enough    
        if len(input_key) >= 20 and any(c.isalpha() for c in input_key) and any(c.isdigit() for c in input_key) and any(c.islower() 
        for c in input_key) and any(c.isupper() for c in input_key):
            salt = bcrypt.gensalt()
            hashed = bcrypt.hashpw(input_key.encode(), salt)
            hashed_keys.append(hashed)
            print("Safe key hashed")
        
        else: # Strong password checker loop
            print("Key is not secure enough, please enter another safer")
# Show crypted keys
if hashed_keys:
    print("Hashed keys:")
    for key in hashed_keys:
        print(key)

if __name__ == "__main__":
    main()
