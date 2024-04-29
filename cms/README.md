# Content Management System (CMS) Design Documentation

### System Architecture Diagrams

**Overview**: 
The system architecture diagram visually represents how the various components of the CMS interact. It includes the client layer, server layer, and database layer, showing how they communicate and collaborate to deliver functionality.

**Components**:
1. **Client Layer** (Front-end): Built with HTML, CSS, and JavaScript, it interacts with the server via RESTful APIs. This layer presents the user interface and handles user inputs and outputs.
2. **Server Layer** (Back-end): Responsible for processing data, managing requests from the client layer, and performing operations like CRUD (Create, Read, Update, Delete) on the database. This layer can be implemented in PHP, Node.js, or Python and includes business logic, authentication, and session management.
3. **Database Layer**: Stores all persistent information such as user data, posts, and configuration settings. This layer is implemented using relational databases like MySQL or PostgreSQL.

**Interactions**:
- Users send requests from the client layer, which are processed by the server layer.
- The server layer retrieves or modifies data in the database layer based on the request.
- Responses are sent back to the client layer to update the user interface accordingly.

![wordpress-site-structure](https://github.com/Digvijayhj/CSC581-Advanced-Software-Engineering/blob/master/cms/1050px-wp_27_modules.jpg?raw=true)

### Scalability and Security
- **Microservices architecture** for scalability.
- **Secure connections** and **JWT** for authentication.

### Database Schema Diagrams

**Overview**:
The database schema diagram provides a detailed view of the tables, their fields, relationships, and how they are indexed in the CMS database.

**Tables**:
1. **Users**: Stores user credentials and profile information.
   - Fields: ID, Username, Email, Password, Role
2. **Posts**: Holds content created by users.
   - Fields: ID, Title, Content, AuthorID (FK), Timestamp
3. **Categories**: Categorizes content into different topics.
   - Fields: ID, CategoryName
4. **Permissions**: Manages access control based on user roles.
   - Fields: RoleID, PermissionType

#### Relationships:
- **Users to Posts**: One-to-many (a user can have multiple posts).
- **Posts to Categories**: Many-to-many (implemented via a post_categories join table).
- **Users to Roles**: Many-to-one (a user has one role, but a role can be assigned to many users).

[er-diagram]!(https://github.com/Digvijayhj/CSC581-Advanced-Software-Engineering/blob/master/cms/erd-wordpress.png?raw=true)

### API Documentation

**Overview**:
The API documentation details each endpoint, describing its purpose, required inputs, returned outputs, and potential error messages.

**Endpoints**:
- **/api/posts**:
  - `GET`: Returns a list of posts. Query parameters can include `page` for pagination and `category` for filtering by category.
  - `POST`: Accepts a JSON object with `title`, `content`, and `category_ids`. Returns the created post with a 201 status code.

- **/api/posts/{id}**:
  - `GET`: Returns a detailed view of a post specified by `id`.
  - `PUT`: Accepts a JSON object with any of `title`, `content`, or `category_ids` to update an existing post. Returns the updated post.
  - `DELETE`: Deletes a post specified by `id`. Returns a 204 status code for successful deletion.


### UI Wireframes and Descriptions

**Overview**:
UI wireframes provide a visual mockup of the CMS interface, showing the layout and interaction elements.

**Key Interfaces**:
1. **Login Page**: Contains fields for username and password, with a submit button for logging in.
2. **Dashboard**: Displays an overview of recent posts, a navigation menu, and a quick draft box.
3. **Content Editor**: Features a rich text editor for writing or editing posts, with options to add images, links, and format text.
4. **Content Management**: Shows a list of all posts with options to edit, delete, or filter them based on categories.

[wireframe-of-wordpress]!(https://github.com/Digvijayhj/CSC581-Advanced-Software-Engineering/blob/master/cms/wordpress-site-structure1%20(1).jpg?raw=true)

[wireframe-flow]!(https://github.com/Digvijayhj/CSC581-Advanced-Software-Engineering/blob/master/cms/wireframe-library-insert.gif?raw=true)

[wirefram-example]!(https://github.com/Digvijayhj/CSC581-Advanced-Software-Engineering/blob/master/cms/Screen-Shot-2021-07-16-at-5.50.57-PM-min-1024x598.png?raw=true)

## Security Considerations

### Threats and Mitigations
- **SQL Injection**: Use prepared statements.
- **Cross-Site Scripting (XSS)**: Sanitize inputs and encode outputs.
- **Data Breaches**: Encrypt sensitive data and implement access controls.