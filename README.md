# E-Book Borrowing System

---

This document is also available in [Chinese](README_CN.md).

---

Your team has been tasked with developing an application that allows people to borrow e-books from a centralized database. The application can be either a website or an actual mobile or desktop application.

## Basic Requirements
The implemented system should have the following features:

- Functionality for users to create and manage accounts.
- Each e-book can only be borrowed by x people for a duration of y.
  - Your team will create virtual e-books with authors, titles, quantity x, and borrowing time y.
- Each account can borrow up to 10 books at a time.
- Create an account dashboard for users to create book wishlists, cancel borrowings, and change login details.
- Provide customers with the functionality to send emails when borrowing or canceling e-books, and send reminders when e-book borrowing is about to end.
- Allow users to leave comments on e-books they have borrowed.
- These requirements should be refined by your team into a set of deliverables. The team is expected to deliver all basic requirements.

## Assumptions

- Only users with accounts can borrow e-books.
  - Browsing the catalog does not require an account.
- No fines - borrowed e-books will be removed from the user's current active e-book list after the borrowing time expires.
- The system should track all e-books borrowed by users.
- The application should include a cover image for each e-book along with its category (such as science fiction, mystery, non-fiction, etc.) and a brief description.

## Possible Extensions

You may want to consider some extensions, such as:

- Providing a payment mechanism for users to borrow e-books. You can use the virtual payment system [HorsePay](http://homepages.cs.ncl.ac.uk/daniel.nesbitt/CSC8019/HorsePay), which simulates users paying with their cards.
- Including visualizations such as tag clouds for book categories.
- Allowing users to post their e-book reviews on social media (such as Facebook).
- Creating functionality for administrators to add/delete/adjust borrowable e-books.

If your team has other extensions, please confirm with Dan or John whether these extensions are appropriate before beginning implementation.

---
POST method parameters use **JSON** format
---
# Authentication
- **JWT Bearer Token** is used for authenticated endpoints.
- Obtain a token via `/api/auth/login`.
---

## [Authentication & User Management](Users.md)
## [E-Book Management](eBooks.md)
## [E-Book Categories](Categories.md)
## [Borrowing System](Borrow.md)
## [Wishlist](Wishlist.md)
## [Shopping Cart](ShoppingCart.md)
## [Review System](Reviews.md)
## [Payment System](Payments.md)

