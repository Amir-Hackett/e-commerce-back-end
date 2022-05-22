# E-commerce Back End

## Description

*Build the back end for an e-commerce site. Take a working Express.js API and configure it to use Sequelize to interact with a MySQL database.*

## Contents
* [Usage](#Usage)
* [Video Description](#Video-Description)
* [Database Models](#Database-Models)
* [Instructions](#Instructions)
* [Installation](#Installation)
* [Built With](#Built-With)
* [Credits](#Credits)

## Usage

GIVEN a functional Express.js API
- WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
  - THEN I am able to connect to a database using Sequelize
- WHEN I enter schema and seed commands
  - THEN a development database is created and is seeded with test data
- WHEN I enter the command to invoke the application
  - THEN my server is started and the Sequelize models are synced to the MySQL database
- WHEN I open API GET routes in Insomnia for categories, products, or tags
  - THEN the data for each of these routes is displayed in a formatted JSON
- WHEN I test API POST, PUT, and DELETE routes in Insomnia
  - THEN I am able to successfully create, update, and delete data in my database

## Video Description

- Tags



https://user-images.githubusercontent.com/99042050/169711264-03d302d4-da2b-45a6-af21-6855b249088a.mp4



- Categories


https://user-images.githubusercontent.com/99042050/169711266-b3a046bf-9444-4ffd-92a6-cd54946a08f4.mp4



- Products


https://user-images.githubusercontent.com/99042050/169711272-476ca3c7-ef96-4788-ae4c-0d474085be8c.mp4


## Database Models

- `Category`

    - `id`
        - Integer
        - Doesn't allow null values
        - Set as primary key
        - Uses auto increment

    - `category_name`
        - String
        - Doesn't allow null values

- `Product`

    - `id`
        - Integer
        - Doesn't allow null values
        - Set as primary key
        - Uses auto increment

    - `product_name`
        - String
        - Doesn't allow null values

    - `price`
        - Decimal
        - Doesn't allow null values
        - Validates that the value is a decimal

    - `stock`
        - Integer
        - Doesn't allow null values
        - Set a default value of 10
        - Validates that the value is numeric

    - `category_id`
        - Integer
        - References the category model's id

- `Tag`

    - `id`
        - Integer
        - Doesn't allow null values
        - Set as primary key
        - Uses auto increment

    - `tag_name`
        - String

- `ProductTag`

    - `id`
        - Integer
        - Doesn't allow null values
        - Set as primary key
        - Uses auto increment

    - `product_id`
        - Integer
        - References the product model's id

    - `tag_id`
        - Integer
        - References the tag model's id

## Built With
* MySQL 2
* Node.js
* Express.js
* Sequelize
* Dotenv
* JavaScript


## Instructions

- Add a .env file to the root of the app with the following details

```text
DB_NAME='ecommerce_db'
DB_USER='root'
DB_PW='xxx'
```
## Installation
Node.js and MySQL are required

Install dependencies 
```terminal
npm init --y
``` 

Open up MySQL and use 
```terminal
source db/schema.sql
```

Quit MySQL and then run the following in the terminal
```terminal
npm run seed
```
Start the app by running the following in the terminal
```terminal
npm start
```

## Credits
* Created by Amir Hackett
