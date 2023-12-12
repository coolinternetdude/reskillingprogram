# reskillingprogram

UML Class diagram



Book Table {
	BookId : int PRIMARY KEY,
	ISBN : VARCHAR(255),
	Title : VARCHAR(255),
	price : DECIMAL(10, 2),
	FOREIGN KEY (CategoryID) REFERENCES Categories(CategoryID)
	DatePublication : DATE,
	DateCreation : DATE,
	Author: Author
}

Categories Table {
	CategoryId: INT PRIMARY KEY,
	Name : VARCHAR(255),
}


Author Table {
	AuthorID: int PRIMARY KEY,
	FullName: VARCHAR(255),
	Description: VARCHAR(255),
}

Inventory Table {
	FOREIGN KEY (BookID) REFERENCES Book(BookID),
}

User Table {
	UserID: int PRIMARY KEY,
	Username: VARCHAR(255),
	Password: VARCHAR(255),
	Email: VARCHAR(255),
}

Role Table {
	RoleID: Int PRIMARY KEY,
	Name: VARCHAR(255),
}

UserRoles Table {
	FOREIGN KEY(RoleID) REFERENCES Role(RoleID),
	FOREIGN KEY(UserID) REFERENCES User(UserID),
}

