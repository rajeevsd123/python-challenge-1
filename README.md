# python-challenge-1
This python program is to allow customers to place an order.
This includes 
 -  Storing the customer's order and 
 - Printing the receipt with the total price of all items ordered.

## Usage

 The following menu will be presesened to a customer 

        1: Snacks

        2: Meals

        3: Drinks

        4: Dessert


Customer needs to enter menu item for the above menu list.

For exmaple if customer inputs "1", following submenu will appear on screen
>
        Item # | Item name                | Price
        -------|--------------------------|-------
        1      | Cookie                   | $0.99
        2      | Banana                   | $0.69
        3      | Apple                    | $0.49
        4      | Granola bar              | $1.99

The customer needs to select the itme from submenu and input the quantity for the order. The quantity will be set to 1 quantiy input is invalid. 

Customer can navigate through menu and submenu list if the customer wants to order more items.
After completing, the order, the customer will be presented with the reciept for the order placed.
For example
> 
    Item name                 | Price    | Quantity
    --------------------------|----------|----------
    Cookie                    | $0.99    | 1
    Pizza - Pepperoni         | $10.99   | 2
    Soda - Small              | $1.99    | 1
    Chocolate lava cake       | $10.99   | 1
    ------------------------------------------------
    Total Price is  $35.95

## About Python program
Python version : 3.10.13

* Data types used :
    Integer, String, Float, Boolean,

    List of Dictionaries: for exmaple

    [

     {
        "Item name": "string",

        "Price": float,

        "Quantity": int
     }
    ]

*   How to navigate through dictionary items? Example:
```python
        for key, value in menu[menu_category_name].items():
                 
                if type(value) is dict:
                    for key2, value2 in value.items():
                        num_item_spaces = 24 - len(key + key2) - 3
                        item_spaces = " " * num_item_spaces
                        print(f"{i}      | {key} - {key2}{item_spaces} | ${value2}")
                        menu_items[i] = {
                            "Item name": key + " - " + key2,
                            "Price": value2
                        }
                        i += 1

```
* Use of append() for order_list
```python
 order_list.append ({
                            "Item Name": menu_item_name_selected,
                            "Price":float (menu_items[int(menu_selection)]['Price']),
                            "Quantity":int(quantity)
                        })
```

* Various control loops /decision statements are used in this program
    
     While loop

     for loop 

     if - else

     match - case 


*f string, exmaple
```python
print(f"{menu_category} was not a menu option.")
```    

* List comprehension is used to calculate total price
```python
 Total_Price = sum((item["Price"])*item["Quantity"]for item in order_list)
 ```
* Used various prompt messages / error messages to interact with user.
 For exaple
```python
print("input isn't valid")
keep_ordering = input("Would you like to keep ordering? (Y/y)es or (N/n)o ")
```


