# API Requirements

The stakeholders are building an online storefront to showcase products. Users need to browse all products, view details of specific products, and add items to orders for review on a cart page. The API should provide endpoints to list all products, view product details, and create new products. Similarly, it should support user operations, including listing users, fetching user details, creating new users, and authenticating users with secure credentials. Additionally, the API must manage orders, allowing users to fetch their current active orders or view completed orders. These endpoints will ensure seamless interaction between the frontend and backend for the application.

These are the notes from a meeting with the frontend developer that describe what endpoints the API needs to supply, as well as data shapes the frontend and backend have agreed meet the requirements of the application.

## API Endpoints

#### Products

- Index: 'products/' [GET]
- Show: 'products/:id' [GET]
- Create [token required]: '/products' [POST]
- Update [token required]: '/products' [PUT]
- Delete [token required]: '/products/:id' [DELETE]

#### Users

- Index [token required]: '/users' [GET]
- Show [token required]: '/users/:id' [GET]
- Create N[token required]: '/users' [POST]
- Update [token required]: '/users' [PUT]
- Delete [token required]: '/users/:id' [DELETE]
- Authenticate [token required]: '/users/authenticate' [POST]

#### Orders

- Current Order by user (args: user id)[token required]: '/orders/:id' [GET]
- Index [token required]: '/orders' [GET]
- Create N[token required]: '/orders' [POST]
- Update [token required]: '/orders' [PUT]
- Delete [token required]: '/orders/:id' [DELETE]

## Data Shapes

#### Product

- id
- name
- price
- [OPTIONAL] category

Table: products (
id serial [primary key],
name varchar(1000) [not null],
price integer [not null]
);

#### User

- id
- firstName
- lastName
- password

Table: users (
id serial [primary key],
username varchar(250) [not null],
firstname varchar(250) [not null],
lastname varchar(250) [not null],
password varchar(1000) [not null]
);

#### Orders

- id
- id of each product in the order
- quantity of each product in the order
- user_id
- status of order (active or complete)

Table: orders (
id serial [primary key],
product_id integer [not null] (product table foreign key),
quantity integer [not null],
user_id integer [not null] (user table foreign key),
status varchar(200) [not null]  
);

#### Order Products

- id of order
- id of each product in the order
- quantity of each product in the order

Table: order_products (
order_id integer [not null] (order table foreign key),
user_id integer [not null] (order table foreign key),
product_id integer [not null] (product table foreign key),
quantity integer [not null]
);
