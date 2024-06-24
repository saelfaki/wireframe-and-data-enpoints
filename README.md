# wireframe-and-data-enpoints
Wireframes:
![SCHOLAR NET-1](https://github.com/saelfaki/wireframe-and-data-enpoints/assets/170651500/f7d64937-b636-485d-97bc-2ecb1d1a2448)
![SCHOLAR NET-2](https://github.com/saelfaki/wireframe-and-data-enpoints/assets/170651500/89b18608-f564-44c6-9a5c-dd11acfa9c65)
![SCHOLAR NET-3](https://github.com/saelfaki/wireframe-and-data-enpoints/assets/170651500/888373ba-ca00-4a68-8089-d597cdf5a9cc)
![SCHOLAR NET-4](https://github.com/saelfaki/wireframe-and-data-enpoints/assets/170651500/bd00b03d-4ee6-4c32-ab7f-bce5eff73abc)
![SCHOLAR NET-5](https://github.com/saelfaki/wireframe-and-data-enpoints/assets/170651500/99452508-8708-4b11-aa38-155a519d5b8f)

Endpoints and Data Model

Data Model:
Profile Attributes: 
id (integer)
username (text)
password(text)
email (text)
bio (text)
role (text: student or benefactor)

Post Attributes:
id (integer)
user_id (integer - foreign key to User)
content (text)
Interview location (text, optional)
created_at (datetime)
updated_at (datetime)

Friends Attributes:
id (integer)
user_id (integer - foreign key to User)
friend_id (integer - foreign key to User)(user who is being added as a friend)
created_at (datetime)

Like Attributes:
id (integer)
 user_id (integer - foreign key to User)
post_id (integer - foreign key to Post)
created_at (datetime)

Endpoints:
GET/posts: Fetches a feed of posts from friends and followed users.

POST/posts: Creates a new post.

PUT/posts/{post_id}: Updates an existing post.

DELETE/posts/{post_id}: Deletes a specific post

POST/friends/{user_id}: Adds a user as a friend.

DELETE/friends/{user_id}: Removes a user from friends list.

POST/posts/{post_id}/like: Likes a specific post.

GET/profile: Retrieves the user's profile information.

POST/profile: Creates a new user account.

PUT/profile: Updates a user's account.
