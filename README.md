# reskillingprogram

UML Class diagram

class User {
userId: int(primary_key),
username: string,
password: string,
isAdmin: boolean,
email: string
}

class Book {
bookId: int(primary_key) // depends if ISBN is unique then no need for bookId ???
Title : string,
Author: string,
ISBN: Long | String (depends if we are going to include the - is going to be a string otherwise long ???);
price: float,
quantity: int,
category : string (or possibly enum so we can limit what the user can choose to avoid having endless categories ????)
}
