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

## Data Models
* Book {
    title, book_id, format, author, publish_year, availability, price, num_pages, publisher, supplier, rating, review, recommendation_score
}

* User {
    name, user_id, year_joined, BookShelf, ShoppingCart, BookClub[], BookChat[]
}

* Bookshelf {
    user_id, Book[]
}

* ShoppingCart {
    user_id, Book[], total_price, num_items
}

* BookClub {
    club_id, User[], Book[], Address[]
}

* BookChat {
    chat_id, book_id, User[]
}

* Rating {
    user_id, book_id, rating_id, date, number
}

* Review {
    user_id, book_id, rating_id, date, text
}

* Order {
    user_id, Book[], date, delivery_status, payment_status
}

## Controller / Functionality
* Book: createNewBook, createNewFormat, changeAvailability, updateBook, deleteBook
* User: registerNewuser, loginUser, logoutUser, updateUserProfile
* Bookshelf: addBookToShelf, removeBookFromShelf
* ShoppingCart: addBookToCart, removeBookFromCart
* BookClub: createNewBookClub, addMemberToBookClub, removeMemberFromBookClub, addBookToBookClub, removeBookFromBookClub
* BookChat: createNewBookChat, addMemberToBookChat, removeMemberFromBookChat
* Rating: createNewRating, updateRating, removeRating
* Review: createNewReview, updateReview, revoveReview
* Order: createNewOrder, updateOrderItems, updateDeliveryStatus, updatePaymentStatus

## DESIGN DOC DETAILS
