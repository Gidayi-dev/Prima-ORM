# Prisma ORM
## ORM
ORM allows developers to interact with databases rather than using sql queries
 (checkout drizzle)
 ## Benefits
 Productivity
 Portability (easier to switch databases)
 Security (SQL injection)
 Maintenance 

 ## Prisma
 Responsible for sql queries
 Provides a type-safe, auto-completion-enabled data mode, automated migrations, and a powerful query builder. Prisma also includes tools like Prisma Studio for data exploration and manipulation, and Prisma Accelerate for optimizing database performance.

(package.JSON file fast (```npm init -y```))
 Install prisma
 ```npm install prisma -D``` on cmd or ```npm install prisma --save-dev``` (used this)

prisma uses postgresql by default so setting up the project (database)
```npx prisma init``` (contains .schema)
On the .env file edit to your own details (postgres: name, password, localhost, name of your database) then save.

 Create models
 Models represent different tables in your database
 ## Prisma models
 Data models
 Field Types 
 Relations
 Attributes

 on schema.prisma
 example
 ```
 model Product {
    id Int @id @default(autoincrement())
    productTitle String
    productDescription String
    productCost Float
    unitsLeft Int

    @@map("products_table") //helps us map it to our database
 }

 //(always make sure you have an id (@id))
 ```
 Migration
 Run a migration
 ```npx prisma migrate dev --name (name of the migration)```

 ```npx prisma migrate dev --name (rename-columns...)```

 Prisma Client
 Provides a simple an intuitive and type safe APIS For CRUD operations
 ```npx prisma generate``` @prisma/client should be automatically added if not manually install using this command
 ```npm install @prisma/client```
 Now on index.js import {prismaClient} from prisma then write your code to create the product ("table values")
 you can check it out on your sql shell
  CRUD OPERATIONS HELPS IN SUCCESS OF THE CODE (index.js) 
  ### CRUD OPERATIONS
  * Create
  * Read
  * Update
  * Delete
  Examples of commands used: 
  * findMany()
  * findFirst()

## Relationship
In Prisma ORM, relationships define how different data models (tables) relate to each other. This allows you to query data across tables efficiently.
* # One-to-one-relationships
This is where a record in one table is associated with one and only one record in another table. Think of it like a passport for a person—each person has exactly one passport.
* # One-to-many relationships
Here, a single record in one table can be associated with multiple records in another table. Imagine a blog post and its comments. One blog post can have many comments.
  









 
