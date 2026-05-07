# Personal Blog

### Functional Requirements
- Users can read the blog posts.
- Users can write the blog posts.
- Users can comment on the blog posts. 

### Non-functional Requirements

- The system should be highly consistent and durable, prioritizing consistency. 
- The systems' APIs should be low latency, reponding the blog post in under 500 ms. 

### Core Entities

- Users
- Blog Posts
- Comments 

### API

*Users Auth Services*
| Method | Endpoint | Body | Description | Access |
| :--- | :--- | :--- | :--- |
| `POST` | `api/auth-service/register/` |  | Users can register to read and write blog posts | Public |
| `POST` | `api/auth-service/login/` |  | Users can get the JWT token | Public |

*Post Services*
| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `POST` | `api/posts-service/posts/` | Users can create and share their blog posts | Private |
| `GET' | `api/posts-service/posts/limit=10&offset=20` | Users can see all the posts at the home page | Public |
| `GET' | `api/posts-service/posts/{post_id}/` | Users can look for and read a post by its ID | Public |

*Comment Services*
| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `POST | `api/comments-service/v1/posts/{post_id}/comments/` | Users can create a comment for a post | Private |
| `GET` | `api/comments-service/v1/posts/{post_id}/comments/{comment_id}/` | Users can read a comment by id | Public | 

### High Level Design





