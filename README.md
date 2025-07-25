## JPA Hibernate Example ##

This project demonstrates how to perform CRUD operations on countries and regions tables using JPA (Jakarta Persistence API) with Hibernate as the provider and PostgreSQL as the database.

It uses:-

Java 23

Hibernate ORM 7

Jakarta EE 11 (jakarta.persistence)

PostgreSQL 15+

Maven for dependency management

## 📂 Project Structure ##

src/

├── main/

│   ├── java/

│   │   ├── app/              # Main application classes

│   │   ├── service/          # Service classes for CRUD

│   │   └── entity/           # JPA Entity classes (Country, Region)

│   └── resources/

│       └── META-INF/

│           └── persistence.xml

└── test/

## 📦 Maven Dependencies ##

The project uses the following dependencies in pom.xml:-

<dependencies>
   
    <dependency>
        
        <groupId>org.hibernate.orm</groupId>
        
        <artifactId>hibernate-core</artifactId>
    
    </dependency>
    
    <dependency>
        
        <groupId>jakarta.persistence</groupId>
        
        <artifactId>jakarta.persistence-api</artifactId>
    
    </dependency>
    
    <dependency>
        
        <groupId>org.postgresql</groupId>
        
        <artifactId>postgresql</artifactId>
        
        <version>42.7.7</version>
    
    </dependency>

</dependencies>

## 🗄 Database Schema ##

## Regions Table ##

CREATE TABLE regions (
   
   region_id SERIAL PRIMARY KEY,
    
    region_name VARCHAR(50) NOT NULL
);

## Countries Table ##

CREATE TABLE countries (
    
    country_id SERIAL PRIMARY KEY,
    
    country_name VARCHAR(50) NOT NULL,
    
    region_id INT REFERENCES regions(region_id)
);

## ⚙️ Setup Instructions ##

1. Clone the repository 

git clone https://github.com/your-username/jpa-hibernate-example.git

cd jpa-hibernate-example

2. Configure Database

Create a PostgreSQL database:

CREATE DATABASE newDB;

Update database credentials in Java files:

<property name="javax.persistence.jdbc.url" value="jdbc:postgresql://localhost:5432/newDB"/>

<property name="javax.persistence.jdbc.user" value="postgres"/>

<property name="javax.persistence.jdbc.password" value="sakshi"/>

## 🖥 Example Menu ##

1. Add Region
2. Add Country
3. View Regions
4. View Countries
5. Exit

## ✅ Features ##

* Add/View countries and regions

* PostgreSQL database integration

* JPA-based persistence layer

* Hibernate as JPA provider

## 📞Contact:- ##

For any questions or feedback, feel free to reach out:

Your Name : sakshi shipkule

Email: shipkulesakshi682@gmail.com

GitHub: Shipkule-Sakshi

## Output ScreenShort:- ##

<img width="1202" height="707" alt="Screenshot 2025-07-14 204948" src="https://github.com/user-attachments/assets/38146a27-8d06-48db-b5e2-e8c9b19da4c6" />

<img width="1379" height="717" alt="Screenshot 2025-07-14 205017" src="https://github.com/user-attachments/assets/39f367ba-e3c5-4952-b80d-abb9560251a8" />

<img width="1390" height="725" alt="Screenshot 2025-07-14 205108" src="https://github.com/user-attachments/assets/f95500be-8f31-417e-8d92-c67dc0f78db6" />






