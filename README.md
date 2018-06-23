# Item Catalog
>a web application that provides a list of items within a variety of categories and integrate third party user registration and authentication. Authenticated users should have the ability to post, edit, and delete their own items.
  
## Getting Started
 * Run vagrant up to run the virtual machine, then vagrant ssh to login to the VM
 * Open up a terminal
 * in the virtual machine  do the following
 ``` 
       -  $ cd /vagrant 
       -  $ cd catalog
       -  $ python application.py
      
```
*  go to http://localhost:5000 to access the application 
## JSON Endpoints
> /restaurant/JSON returns all restaurant 
```
  {
  "restaurants": [
    {
      "id": 1, 
      "name": "Urban Burger"
    }, 
    {
      "id": 2, 
      "name": "Super Stir Fry"
    ]
    }
    
```
>/restaurant/<int:restaurant_id>/menu/JSON return menu of restaurant specified
```
{
  "MenuItems": [
    {
      "course": "Entree", 
      "description": "Marinated Pork, Rice, Beans, Avocado, Cilantro, Salsa, Tortilla", 
      "id": 44, 
      "name": "Super Burrito Al Pastor", 
      "price": "$5.95"
    }, 
    {
      "course": "Entree", 
      "description": "Golden brown, corn-based Venezuelan pancake; usually stuffed with queso telita or queso de mano, and possibly lechon. ", 
      "id": 45, 
      "name": "Cachapa", 
      "price": "$7.99"
    }
  ]
}
```
>/restaurant/<int:restaurant_id>/menu/<int:menu_id>/JSON return specified menu
```
{
  "Menu_Item": {
    "course": "Entree", 
    "description": "Juicy grilled veggie patty with tomato mayo and lettuce", 
    "id": 1, 
    "name": "Veggie Burger", 
    "price": "$7.50"
  }
}
```
## Prerequisites
* python version 3.6.2 
* Vagrant
* Virtual machine
