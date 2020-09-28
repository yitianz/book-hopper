# Engineering Requirements Document

## Modules
* Search
* Recommendation
* Bookshelf
* Purchasing
* Payments
* Ratings
* Social feed
* Book club / chat

## Data Model
* Book {
    title,
    book_id, 
    format,
    author, 
    publish_year, 
    availability,
    price,
    num_pages,
    publisher,
    supplier
}

* User {
    name,
    user_id,
    year_joined,
    bookshelf,
    shopping_cart,
    book_clubs,
    book_chats
}

* Bookshelf {
    user_id, 
    Book[]
}

* ShoppingCart {
    user_id,
    Book[]
}

* BookClub {
    club_id,
    User[],
    Book[],
    Address[]
}

* BookChat {
    chat_id,
    book_id,
    User[]
}
