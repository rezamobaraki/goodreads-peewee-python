## Goodreads Database System with Peewee ORM

A Python-based Goodreads-like book management system built with Peewee ORM. This project demonstrates database design and ORM usage for managing books, authors, users, and reading lists.

Created by [Reza Mobaraki](https://www.linkedin.com/in/reza-mobaraki/)

## 🚀 Features

- **User Management**: User registration, authentication, and profiles
- **Book Management**: Book catalog with ISBN tracking
- **Author Management**: Author profiles and book associations  
- **Reading Lists**: Customizable shelves (read, currently reading, want to read)
- **Book Reviews**: Rating and commenting system
- **Social Features**: User following and author following
- **Data Import**: JSON-based fixture system for sample data

## 📚 Table of Contents

* [Features](#-features)
* [Technologies](#-technologies)
* [Database Schema](#-database-schema)
* [Setup](#-setup)
* [Usage](#-usage)
* [Project Structure](#-project-structure)
* [Contributing](#-contributing)
* [Credits](#credits)
* [Contributors](#contributors)
* [License](#license)

## 🛠 Technologies

Project is built with:

* **Python**: 3.9+
* **Peewee ORM**: 3.14+ - Lightweight Python ORM
* **MySQL**: Database backend
* **JSON**: Fixture data format

## 🗄 Database Schema

The project implements a comprehensive book management database with the following models:

- **User**: User accounts with authentication
- **Book**: Book catalog with ISBN and metadata
- **Author**: Author information and relationships
- **Shelf**: User-defined book collections
- **BookShelf**: Many-to-many relationship between books and shelves with ratings/comments
- **BookAuthor**: Many-to-many relationship between books and authors
- **BookTranslator**: Book translation relationships
- **UserAuthorRelation**: User following authors
- **UserRelation**: User following other users

## 🔧 Setup

### Prerequisites

- Python 3.9 or higher
- MySQL server
- pip package manager

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/rezamobaraki/goodreads-peewee-python.git
cd goodreads-peewee-python
```

2. **Create virtual environment**
```bash
python3 -m venv venv
# or
virtualenv -p python3 venv 
```

3. **Activate virtual environment**
```bash
# On Linux/Mac
source venv/bin/activate  

# On Windows
venv\Scripts\activate
```

4. **Install dependencies**
```bash
pip install -r requirements.txt
```

5. **Configure Database**
   - Create a MySQL database named `goodreads2`
   - Update database credentials in `models.py` if needed
   - Default configuration: `mysql://goodreads:goodreads@localhost/goodreads2`

6. **Run the application**
```bash
python main.py
```

## 💻 Usage

The application loads sample data from JSON fixtures and demonstrates various database operations:

- User management and authentication
- Book and author data import
- Shelf creation and book organization
- Reporting functions for users and books

### Sample Data

The project includes fixture files in the `fixtures/` directory:
- `users.json` - Sample user accounts
- `books.json` - Book catalog
- `authors.json` - Author information
- `books-authors.json` - Book-author relationships
- `books-shelves.json` - User book shelves and ratings

## 📁 Project Structure

```
goodreads-peewee-python/
├── fixtures/           # Sample data files
│   ├── users.json
│   ├── books.json
│   ├── authors.json
│   ├── books-authors.json
│   ├── books-shelves.json
│   └── reports.py      # Database reporting functions
├── models.py           # Database models and schema
├── importer.py         # Data import utilities
├── main.py            # Main application entry point
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation
```

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements or modern technologies to integrate:

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Your contributions will be acknowledged in the credits and contributors section.

## Credits

* [7learn](https://www.7learn.ac/)

## Contributors

* [rezamobaraki](https://github.com/rezamobaraki)

## License

Distributed under the MIT License. See [license](LICENSE) for more information.
