# MyContacts API

This repository contains the MyContacts API, developed as part of the JStack Course. It is a powerful and efficient solution for managing contact information. With a comprehensive set of functions including create, read, update, and delete operations, the MyContacts API simplifies the management of contact records.

## Features

- **Create**: Easily create new contact records with relevant details such as name, email, phone number, and more.
- **Read**: Retrieve contact information using various search parameters, enabling quick and precise access to the desired records.
- **Update**: Seamlessly update existing contact records, ensuring accurate and up-to-date information.
- **Delete**: Effortlessly remove unwanted contact records, maintaining data integrity.

## Technologies Used

- **Node.js**: The MyContacts API is developed using Node.js, a powerful and versatile runtime environment for server-side applications.
- **Express**: Built with Express, a fast and minimalistic web application framework for Node.js, the MyContacts API ensures efficient routing, middleware integration, and request handling.
- **PostgreSQL**: The API uses a PostgreSQL database to store contact and category data.

## Getting Started

To set up and run the MyContacts API locally, follow these steps:

1. Clone this repository: `git clone <repository-url>`
2. Navigate to the project directory: `cd mycontacts-api`
3. Install the dependencies: `npm install`
4. Set up a PostgreSQL database and run the SQL queries from the `database.sql` file to create the necessary tables.
5. Configure the database connection in the `database.js` file.
6. Start the server: `npm run dev`
7. The API will be accessible at `http://localhost:3000`.

## API Endpoints

The MyContacts API exposes the following endpoints:

- `POST /contacts`: Create a new contact.
- `GET /contacts`: Retrieve all contacts.
- `GET /contacts/:id`: Retrieve a specific contact by ID.
- `PUT /contacts/:id`: Update a specific contact by ID.
- `DELETE /contacts/:id`: Delete a specific contact by ID.
- `GET /categories`: Retrieve all categories.
- `POST /categories`: Create a new category.

Please note that the MyContacts API now uses a PostgreSQL database for data storage.

## Controllers

The API controllers handle the logic for each endpoint. The following controllers are included:

- `ContactController`: Manages the contact-related endpoints.
- `CategoryController`: Manages the category-related endpoints.

## Repositories

The API repositories interact with the database to perform CRUD operations. The following repositories are included:

- `ContactsRepository`: Handles database operations for the contact entity.
- `CategoriesRepository`: Handles database operations for the category entity.

## Database Setup

To use the MyContacts API with a database, you need to set up a PostgreSQL database and run the following SQL queries:

```sql
CREATE DATABASE mycontacts;

CREATE EXTENSION IF NOT EXISTS "uuid-ossp";

CREATE TABLE IF NOT EXISTS categories (
  id UUID NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
  name VARCHAR NOT NULL
);

CREATE TABLE IF NOT EXISTS contacts (
  id UUID NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
  name VARCHAR NOT NULL,
  email VARCHAR UNIQUE,
  phone VARCHAR,
  category_id UUID,
  FOREIGN KEY(category_id) REFERENCES categories(id)
);
```

Usage with Database
To use the MyContacts API with a database, you need to make the following changes to the code:

Update the database connection details in the database.js file.
Remove the mock data and use the PostgreSQL database tables contacts and categories for data storage.
Installation and Running the API
Clone this repository: git clone https://github.com/oleonardodeandrade/mycontacts_jstack
Navigate to the project directory: cd mycontacts_jstack
Install the dependencies: npm install
Set up a PostgreSQL database and run the SQL queries from the database.sql file to create the necessary tables.
Configure the database connection in the database.js file.
Start the server: npm run dev
The API will be accessible at http://localhost:3000.
Contributing
Contributions to the MyContacts API are welcome and encouraged. To contribute, please follow these guidelines:

Fork this repository.
Create a new branch: git checkout -b my-feature
Make your changes and commit them: git commit -am 'Add new feature'
Push to the branch: git push origin my-feature
Submit a pull request.
License
The MyContacts API is open-source and released under the MIT License. Feel free to modify and use the code in accordance with the terms of the license.

Acknowledgements
The development of the MyContacts API was made possible through the JStack Course. We extend our gratitude to the JStack team for their guidance and support throughout the course.

Contact
If you have any questions, suggestions, or issues, please feel free to reach out to us. You can contact the project maintainers by emailing leonardoh.deandrade@gmail.com or by opening an issue in this repository.
