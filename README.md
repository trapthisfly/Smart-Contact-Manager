# Java Project README

The Smart Contact Manager is a Java-based application designed to efficiently manage contacts and their information. It provides a user-friendly interface for adding, editing, and organizing contacts, ensuring seamless communication and collaboration.

### Technologies Used      
- **Java**: The core programming language used for developing the application.     
- **Maven**: Dependency management tool for building and managing project dependencies.     
- **MariaDB**: Optional database system for storing contact information.   
- **Thymeleaf**: Frontend templating engine for creating dynamic web pages with Java.

- **HTML/CSS/JavaScript**: Frontend technologies for enhancing the user interface.
## Prerequisites

- Java Development Kit (JDK) installed
- Maven installed
- MariaDB Database

## Running the Application

Clone this repository:
```git clone https://github.com/yourusername/your-repository.git```

### MariaDB Database

#### Installation

1. Install MariaDB by following the instructions for your operating system: [MariaDB Installation Guide]https://mariadb.com/kb/en/getting-installing-and-upgrading-mariadb/)


#### Creation of Database

- Open a terminal or command prompt.

 - Log in to the MariaDB server as the root user: ```mariadb -uroot -p```

 -  Enter the root password when prompted.
 - Create a new database for your application: ```CREATE DATABASE digitalcontact;```
 
 - Optionally, you can create a new user and grant privileges to the database: ```CREATE USER 'your_user'@'localhost' IDENTIFIED BY 'your_password';  GRANT ALL PRIVILEGES ON digitalcontact.* TO 'your_user'@'localhost';```
 - If you happen to create user using these commands you need to update the ```src/main/resources/application.properties``` file. You will need to update this file even if you did not create a new user. You can use your existing username and password. You need to update these lines: ```spring.datasource.username='your_user'``` ```spring.datasource.password='your_password'``` 
 ### Running the project
1. Navigate to the project directory:
 - ```cd smartcontactmanager```

2. Build the project using Maven:
 - ```mvn spring-boot:run```
 - If you encounter any errors during installation regarding hibernate then you need to check your ```src/main/resources/application.properties``` file. and double check your entries for username and password.

The application will be accessible at [http://localhost:8081/](http://localhost:8081/).

## Additional Information

- Modify `pom.xml` to add or update dependencies.
- Source code is located in the `src/` directory.
- Compiled classes and JAR file will be generated in the `target/` directory.
- You can change the port at which your application runs too. Just change this: ```server.port=8081``` line in the  ```src/main/resources/application.properties``` 

