# Hacker School News
--

Below there is a description of the project we are going to be building for the next week.

List of features:

1. As a user I can log in with email and password
2. As a user I can log out from the application
3. As a user I can register with my email and password
4. As a user I can post a link
5. As a user I can edit any of my links
6. As a user I can destroy a link
7. As a user I can see a feed of links
8. As a user I can comment on a link
9. As a user I can upvote a link
10. As a user I can downvote a link

Modeling:

```yaml
user:
	email:string
	encrypted_password:string
	devise_stuff...
link:
	title:string
	url:text
	user_id:integer:index
comment:
	user_id:integer:index
	link_id:integer:index
	content:text
vote:
	user_id:integer:index
	link_id:integer:index
	kind:integer -> Enums
```