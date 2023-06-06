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

## Getting Started

To set up and run the MyContacts API locally, follow these steps:

1. Clone this repository: `git clone <repository-url>`
2. Navigate to the project directory: `cd mycontacts-api`
3. Install the dependencies: `npm install`
4. Start the server: `npm start`
5. The API will be accessible at `http://localhost:3000`.

## API Endpoints

The MyContacts API exposes the following endpoints:

- `POST /contacts`: Create a new contact.
- `GET /contacts`: Retrieve all contacts.
- `GET /contacts/:id`: Retrieve a specific contact by ID.
- `PUT /contacts/:id`: Update a specific contact by ID.
- `DELETE /contacts/:id`: Delete a specific contact by ID.

Please note that the MyContacts API currently uses mock data and does not connect to a database. The data is stored in memory during the runtime of the application.

## Mock Data

The MyContacts API uses the following mock data as an example:

```javascript
let contacts = [
  {
    id: v4(),
    name: 'Leonardo',
    email: 'leonardo@gmail.com',
    phone: '1212121',
    category_id: v4(),
  },
  {
    id: v4(),
    name: 'José',
    email: 'jose@gmail.com',
    phone: '1212121',
    category_id: v4(),
  },
];
```

Please note that the `v4()` function is a placeholder representing a unique identifier generator.

For detailed documentation on the API endpoints and their usage, please refer to the API documentation or the source code.

## Contributing

Contributions to the MyContacts API are welcome and encouraged. To contribute, please follow these guidelines:

1. Fork this repository.
2. Create a new branch: `git checkout -b my-feature`
3. Make your changes and commit them: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin my-feature`
5. Submit a pull request.

## License

The MyContacts API is open-source and released under the [MIT License](LICENSE). Feel free to modify and use the code in accordance with the terms of the license.

## Acknowledgements

The development of the MyContacts API was made possible through the JStack Course. We extend our gratitude to the JStack team for their guidance and support throughout the course.

## Contact

If you have any questions, suggestions, or issues

, please feel free to reach out to us. You can contact the project maintainers by emailing [leonardoh.deandrade@gmail.com](mailto:leonardoh.deandrade@gmail.com) or by opening an issue in this repository.
