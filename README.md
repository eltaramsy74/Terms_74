
TERMS_STORE = { "line": ["tokyo", "vape station", "vgod"], "price": [500, 250, 600] }

print("Welcome to the TERMS_STORE")

#Loop until user types 5
while True:
    print("Please choose an option:")
    print("1. Add a liquid")
    print("2. Delete a liquid")
    print("3. Edit a liquid's price")
    print("4. Show all liquids")
    print("5. Exit")

    choose = input("Enter your choose: ").strip()

    if choose == "5":
        print("Thank you for using the TERMS_STORE")
        break
    elif choose == "1":
        line = input("Enter line name: ").lower()
        price = float(input("Enter liquid price: "))
        TERMS_STORE["line"].append(line)
        TERMS_STORE["price"].append(price)
        print("Liquid added success")
    elif choose == "2":
        line = input("Enter liquid name to delete: ").strip().lower()
        to_remove = None # WE USE NONE TO CHEK ELIMINT IN DIC OR NOT AND WE CAN USE -1 BUT WRITE FOUND
        for i in range(len(TERMS_STORE["line"])):
            if TERMS_STORE["line"][i].lower() == line:
                to_remove = i
                break
        if to_remove is not None:
            del TERMS_STORE["line"][to_remove]
            del TERMS_STORE["price"][to_remove]
            print("Liquid deleted success")
        else:
            print("Liquid not found in TERMS_STORE")
    elif choose == "3":
        line = input("Enter liquid name to edit price: ").strip().lower()
        to_edit = None
        for i in range(len(TERMS_STORE["line"])):
            if TERMS_STORE["line"][i].lower() == line:
                to_edit = i
                break
        if to_edit is not None:
            new_price = float(input("Enter new price: "))
            TERMS_STORE["price"][to_edit] = new_price
            print("Price updated success")
        else:
            print("Liquid not found in the store")
    elif choose == "4":
        if TERMS_STORE["line"]:
            print(" All liquids in the Vape Store:")
            for i in range(len(TERMS_STORE["line"])):
                print(f"LINE : {TERMS_STORE['line'][i]} : {TERMS_STORE['price'][i]} L.E")
        else:
            print(" The store is empty")
    else:
        print("Invalid choose,Please enter 1, 2, 3, 4 , 5") #IF USER CHOOSE OUT OF MY LISY
Welcome to the TERMS_STORE
Please choose an option:
1. Add a liquid
2. Delete a liquid
3. Edit a liquid's price
4. Show all liquids
5. Exit
Enter your choose:  1
Enter line name:  TTKKK
Enter liquid price:  123
Liquid added success
Please choose an option:
1. Add a liquid
2. Delete a liquid
3. Edit a liquid's price
4. Show all liquids
5. Exit
Enter your choose:  4
 All liquids in the Vape Store:
LINE : tokyo : 500 L.E
LINE : vape station : 250 L.E
LINE : vgod : 600 L.E
LINE : ttkkk : 123.0 L.E
Please choose an option:
1. Add a liquid
2. Delete a liquid
3. Edit a liquid's price
4. Show all liquids
5. Exit
Enter your choose:  9
Invalid choose,Please enter 1, 2, 3, 4 , 5
Please choose an option:
1. Add a liquid
2. Delete a liquid
3. Edit a liquid's price
4. Show all liquids
5. Exit
Enter your choose:  ~
Invalid choose,Please enter 1, 2, 3, 4 , 5
Please choose an option:
1. Add a liquid
2. Delete a liquid
3. Edit a liquid's price
4. Show all liquids
5. Exit
Enter your choose:  5
Thank you for using the TERMS_STORE
 
