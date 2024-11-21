# Book Pals
CS5200 - Database Management Systems
Project 3 / Library Management System using Node.js, Express, Redis
# Book Swapping Management System 📚🤝

The **Book Swapping Management System** is a platform designed to connect book lovers within the same geographical region, making it easy to share and discover new reads. This system allows users to add, borrow, and rate books while fostering a sense of community among readers.
---

## Features ✨

- **Book Owners**: Add books to share with others in your region.
- **Book Borrowers**: Browse and borrow books available locally.
- **Dual Roles**: Users can act as both book owners and borrowers.
- **Ratings**: Rate books on a 5-star scale after borrowing or lending them.
- **Advanced Search**: Search for books by title, author, genre, or rating (within your region).
- **Genres**: Books are categorized by genre for easy discovery.
---

## Technical Details ⚙️

### Core Functionalities
- **Geographical Regions**: Users are assigned to a specific region and can only borrow books within their area.
- **Loan Management**: Users can own and borrow multiple books, but a single book can only be loaned to one user at a time.
- **Data Consistency**: Borrowed and owned books are tracked to ensure availability.

### Data Management with Redis
We utilized a **Redis Hashmap** data structure to manage user data efficiently. Redis provides fast and scalable operations for creating, searching, updating, and deleting user records.

#### Example Redis Structure:
- **Key**: `user:<user_id>`
- **Fields and Values**:
  - `name`: User's name (e.g., "Jane Doe")
  - `region`: Assigned geographical region (e.g., "North Bay")
  - `borrowed_books`: List of borrowed books (e.g., `["Book1", "Book2"]`)
  - `owned_books`: List of owned books (e.g., `["Book3", "Book4"]`)
  - `ratings`: Dictionary of rated books (e.g., `{"Book1": 5, "Book2": 4}`)

### Search Capabilities
- Searchable fields include:
  - Book title
  - Author
  - Genre
  - Book rating
- Results are filtered by the user’s geographical region.
---

## How It Works 🛠️

1. **Book Owners**:
   - Add books to the system.
   - Track ratings for books they've lent out.

2. **Book Borrowers**:
   - Browse books available in their region.
   - Borrow a book and rate it after returning.

3. **Dual Roles**:
   - Users can manage both owned and borrowed books simultaneously.

4. **Rating System**:
   - Rate books on a 5-star scale to help other users find quality reads.

5. **Search**:
   - Users can search by title, author, genre, or rating within their region.
---

## UML Class Diagram:
![Website Screenshot](https://github.com/greeny90/BookPalsVersion3/blob/main/B%20-%20UML%20Class%20Diagram.png)
## BookPals Home Page:
![Website Screenshot](https://github.com/greeny90/BookPalsVersion3/blob/main/images/home_page.png)
## Search User Page:
![Website Screenshot](https://github.com/greeny90/BookPalsVersion3/blob/main/images/searchresultspage.png)
## Add User Page:
![Website Screenshot](https://github.com/greeny90/BookPalsVersion3/blob/main/images/adduserpage.png)
## RedisInsights-Preview Page:
![Website Screenshot](https://github.com/greeny90/BookPalsVersion3/blob/main/images/RedisInsightspage.png)
# Installation and Setup 🚀
1) Clone the repository
2) Install the dependencies and run `npm install`
3) `npm start`
4) Start Redis server locally: `redis-server`
5) To use the RedisInsight GUI, go to https://docs.redis.com/latest/ri/installing/install-redis-desktop/

# Functions of this application
* This is CRUD application that has the capability of:
* creating users and books
* reviewing users and books
* updating users and books
* deleting users and books

# Future Improvements 🚀
* Extend functionality to include book reviews.
* Add notifications for overdue books.
* Expand geographical filters to allow cross-region borrowing with approval.
* Implement AI-based recommendations based on user preferences and ratings.

# Acknowledgments 🙌
This project was developed to promote community, sustainability, and a shared love for reading. RedisInsight-Preview was instrumental in visualizing and managing our data effectively.
 
## Authors
* Yvette Green
* Semaa Amin

