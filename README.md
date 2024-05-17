# Simple Api

A basic Application with multiple functionalities built with FastAPI aim to help Users Buy New Items Provided by PaypalAPI to Complete the Payment and Check it.

## Getting Started

Simple Api provide a Basic API Compose :

<ol>
    <li>Users</li>
<ol>
        <li>login : <code>http://localhost:8000 user/login</code> </li>
        <li>Register : <code>http://localhost:8000/user/register</code></li>
        <li>Get User : <code>http://localhost:8000/user/get_user/{username}</code></li>
</ol>
    <li>Items</li>
<ol>
        <li>Add Item : <code>http://localhost:8000/item/add_item</code></li>
        <li>Get Item : <code>http://localhost:8000/item/get_item/{id}</code></li>
        <li>Delete Item : <code>http://localhost:8000/item/get_item/{id}</code></li>
</ol>
    <li>Payment</li>
<ol>
        <li>Add Item to Cart : <code>http://localhost:8000/cart/add_to_cart/{username}</code></li>
        <li>Provide Item to Payments : <code>http://localhost:8000/cart/payment</code></li>
        <li>Money Callback : <code>http://localhost:8000/cart/callback</code></li>
        <li>Delete Cart Item : <code>http://localhost:8000/cart/delete_cart_item/{id}</code></li>
</ol>
</ol>

> I pre-configured the Cruds with the payment process based on `PaypalAPI`, you can read the Official docs here [REST APIs / API Requests](https://developer.paypal.com/docs/api/reference/api-requests/)

### Prerequisites

- Python 3.9.2 or higher
- FastAPI

### Project setup

```sh
# clone the repo
$ git clone https://github.com/syd200/SimpleApi.git

# move to the project folder
$ cd SimpleApi
```

### Creating virtual environment
```sh
# creating virtual environment for python 3 using venv
$ python -m venv [env-name]

# activating the virtual environment
$ source [env-name]/bin/activate

# install all dependencies in virtual environment
$ pip install -r requirement.txt
```

### Running the Application

- To run the [Main](main.py) we need to use [uvicorn](https://www.uvicorn.org/) a lightning-fast ASGI server implementation, using uvloop and httptools.

```sh
# Running the application using uvicorn
$ uvicorn main:app

## To run the Application under a reload enviromment use -- reload
$ uvicorn main:app --reload
```