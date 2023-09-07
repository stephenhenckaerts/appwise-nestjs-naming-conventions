# 🌟📚✨ Project Naming Conventions ✨📚🌟

> **TL;DR**: This guide outlines the naming conventions to follow for file naming and function, enhancing readability and consistency throughout the project.

## 🎮 Controllers 

### 📂 File Naming Conventions 

#### 📄 Single Entity 
- **Filename**: `<entity>.controller.ts`
  - 🔍 **Example**: `user.controller.ts`
  
#### 🗂️ Multiple Entities (Relations) 
- **Filename**: `<entity1>-<entity2>.controller.ts`
  - 🔍 **Example**: `user-pet.controller.ts`

### ⚙️ Function Naming Conventions 

#### 🛠️ Creating an Entity 
- **Function Name**: `createOne`
  - 📘 **Description**: Function to create and return a single entity.
  - 🔍 **Example**: createOne

- **Function Name**: `createMany`
  - 📘 **Description**: Function to create and return multiple entities at once.
  - 🔍 **Example**: createMany

#### 🔍 Finding Entities 
- **Function Name**: `findOne`
  - 📘 **Description**: Function to find and return a single entity by its UUID.
  - 🔍 **Example**: findOne

- **Function Name**: `findAll`
  - 📘 **Description**: Function to find and return all entities.
  - 🔍 **Example**: findAll

- **Function Name**: `findOneBy<Property>`
  - 📘 **Description**: Function to find and return a single entity based on a specific property other than UUID (e.g., `findOneByEmail`).
  - 🔍 **Example**: findOneByEmail

#### ♻️ Updating Entities 
- **Function Name**: `updateOne`
  - 📘 **Description**: Function to update and return a single entity by its UUID.
  - 🔍 **Example**: updateOne

- (Optional) **Function Name**: `updateMany`
  - 📘 **Description**: Function to update and return multiple entities based on certain conditions (if applicable).
  - 🔍 **Example**: updateMany

#### 🗑️ Deleting Entities 
- **Function Name**: `deleteOne`
  - 📘 **Description**: Function to delete a single entity by its UUID.
  - 🔍 **Example**: deleteOne

- (Optional) **Function Name**: `deleteMany`
  - 📘 **Description**: Function to delete multiple entities based on certain conditions (if applicable).
  - 🔍 **Example**: deleteMany


---

## 🚀 Services

### 📁 File Naming Conventions

#### 📄 Single Entity
- **Filename**: `<entity>.service.ts`
  - 🔍 **Example**: `user.service.ts` 

#### 💼 Interface for Service
- **Filename**: `<entity>.service.interface.ts`
  - 🔍 **Example**: `user.service.interface.ts` 

#### 🎭 Mock Implementation for Service
- **Filename**: `<entity>.mock.service.ts`
  - 🔍 **Example**: `user.mock.service.ts` 

#### 💑 Multiple Entities (Relations)
- **Filename**: `<entity1>-<entity2>.service.ts`
  - 🔍 **Example**: `user-pet.service.ts` 

### 🎯 Function Naming Conventions

#### 🏗️ Creating an Entity
- **Function Name**: `createOne`
  - 📘 **Description**:: Function to create and return a single entity.
  - 🔍 **Example**: `createOne`

#### 🔍 Finding Entities
- **Function Name**: `findOne`
  - 📘 **Description**:: Finds and returns an entity or `null` if it is being searched by the primary key.
  - 🔍 **Example**: `findOne`

- **Function Name**: `findOne<Property>`
  - 📘 **Description**:: Finds and returns an entity or `null` based on a specific property if not the primary key.
  - 🔍 **Example**: `findOneByEmail`

- **Function Name**: `findOneOrFail`
  - 📘 **Description**:: Similar to the above but throws an error if the entity is not found when searched by the primary key.
  - 🔍 **Example**: `findOneOrFail`

- **Function Name**: `findOne<Property>OrFail`
  - 📘 **Description**:: Similar to `findOne<Property>`, but throws an error if not found.
  - 🔍 **Example**: `findOneByEmailOrFail`

- **Function Name**: `findAll`
  - 📘 **Description**:: Finds and returns all entities.
  - 🔍 **Example**: `findAll`

#### 🛠️ Updating Entities
- **Function Name**: `updateOne`
  - 📘 **Description**:: Updates an entity and returns the updated entity or `null` if it is being updated by the primary key.
  - 🔍 **Example**: `updateOne`

- **Function Name**: `updateOne<Property>`
  - 📘 **Description**:: Updates an entity based on a specific property and returns the updated entity or `null` if not the primary key.
  - 🔍 **Example**: `updateOneByEmail`

- **Function Name**: `updateOneOrFail`
  - 📘 **Description**:: Similar to the above but throws an error if the entity is not found when updated by the primary key.
  - 🔍 **Example**: `updateOneOrFail`

- **Function Name**: `updateOne<Property>OrFail`
  - 📘 **Description**:: Similar to `updateOne<Property>`, but throws an error if not found.
  - 🔍 **Example**: `updateOneByEmailOrFail`

#### 🗑️ Deleting Entities
- **Function Name**: `deleteOne`
  - 📘 **Description**:: Deletes an entity and returns some indication of success or `null` if it is being deleted by the primary key.
  - 🔍 **Example**: `deleteOne`

- **Function Name**: `deleteOne<Property>`
  - 📘 **Description**:: Deletes an entity based on a specific property and returns some indication of success or `null` if not the primary key.
  - 🔍 **Example**: `deleteOneByEmail`

- **Function Name**: `deleteOneOrFail`
  - 📘 **Description**:: Similar to the above but throws an error if the entity is not found when deleted by the primary key.
  - 🔍 **Example**: `deleteOneOrFail`

- **Function Name**: `deleteOne<Property>OrFail`
  - 📘 **Description**:: Similar to `deleteOne<Property>`, but throws an error if not found.
  - 🔍 **Example**: `deleteOneByEmailOrFail`

#### 🤝 Sub-object Operations
- **Function Name**: `findAll<SubObject>For<Object>`
  - 📘 **Description**:: To find all sub-objects for a particular object.
  - 🔍 **Example**: `findAllPetsForUser`

- **Function Name**: `find<Object>By<SubObjectProperty>`
  - 📘 **Description**:: To find an object by a property of its sub-object.
  - 🔍 **Example**: `findOneByPetName`

#### 🌐 Bulk Operations
- **Function Name**: `createMany`
  - 📘 **Description**:: For creating multiple entities at once.
  - 🔍 **Example**: `createMany`

- **Function Name**: `updateMany`
  - 📘 **Description**:: For updating multiple entities at once.
  - 🔍 **Example**: `updateMany`

- **Function Name**: `deleteMany`
  - 📘 **Description**:: For deleting multiple entities at once.
  - 🔍 **Example**: `deleteMany`

#### 🧮 Utilitarian Functions
- **Function Name**: `count`
  - 📘 **Description**:: To count all entities.
  - 🔍 **Example**: `count`
  
- **Function Name**: `countBy<Property>`
  - 📘 **Description**:: To count entities based on a certain property.
  - 🔍 **Example**: `countByEmail`

#### 🔎 Specific Find Operations
- **Function Name**: `findOneBy<Property>And<AnotherProperty>`
  - 📘 **Description**:: For finding entities based on multiple criteria.
  - 🔍 **Example**: `findOneByAgeAndName`

---

## 📦 Repository 

### 📁 File Naming Conventions

#### 📑 Single Entity
- **Filename**: `<entity>.repository.ts`
  - 🔍 **Example**: `user.repository.ts`

#### 📑 Multiple Entities (Relations)
- **Filename**: `<entity1>-<entity2>.repository.ts`
  - 🔍 **Example**: `user-pet.repository.ts`

### 🛠️ Function Naming Conventions

#### 🔍 Complex Find Operations
- **Function Name**: `findWith<Relation>(criteria)`
  - 📘 **Description**: Finds entities with specific relations loaded (e.g., `findWithPets(criteria)`).
  - 🔍 **Example**: findWithPets(criteria)
  
- **Function Name**: `findBy<Property>And<AnotherProperty>(propertyValue1, propertyValue2)`
  - 📘 **Description**: Finds entities based on multiple criteria (e.g., `findByAgeAndGender(age, gender)`).
  - 🔍 **Example**: findByAgeAndGender(age, gender)

#### 📊 Aggregation Operations
- **Function Name**: `countBy<Property>(propertyValue)`
  - 📘 **Description**: Counts entities based on a specific property (e.g., `countByAge(age)`).
  - 🔍 **Example**: countByAge(age)

- **Function Name**: `sum<Property>(propertyValue)`
  - 📘 **Description**: Sums up values of a specific property across all entities (e.g., `sumOrderValue(orderValue)`).
  - 🔍 **Example**: sumOrderValue(orderValue)

#### 📈 Many Operations
- **Function Name**: `createMany(entities)`
  - 📘 **Description**: Creates multiple entities in one operation.
  - 🔍 **Example**: createMany(entities)

- **Function Name**: `updateMany(criteria, updateData)`
  - 📘 **Description**: Updates multiple entities matching the criteria with the specified update data.
  - 🔍 **Example**: updateMany(criteria, updateData)

- **Function Name**: `deleteMany(criteria)`
  - 📘 **Description**: Deletes multiple entities matching the criteria.
  - 🔍 **Example**: deleteMany(criteria)
---

## 📄 Entities

### 📁 File and Class Naming Conventions

#### Single Entity
- **Filename**: `<entity>.entity.ts`
  - 🔍 **Example**: `user.entity.ts`
  
- **Class Name**: Should follow PascalCase and clearly represent the entity being modeled.
  - 🔍 **Example**: `User`, `UserProfile`

### 🖊 Property Naming Conventions

- **Simple Properties**: The names should be concise, meaningful, and follow camelCase.
  - 🔍 **Example**: `firstName`, `emailAddress`

- **Relations**:
  - **One-to-One and Many-to-One**: The property name should be singular and clearly represent the related entity.
    - 🔍 **Example**: `profile`, `address`
  - **One-to-Many**: The property name should be plural and clearly represent the related entities.
    - 🔍 **Example**: `posts`, `comments`
  - **Many-to-Many**: Always create separate entities for each many-to-many relationship.
    - **Example**: `UserAddress`, `GroupMember`

- **Date Properties**: Use "On" to indicate date properties.
  - 🔍 **Example**: `createdOn`, `updatedOn`
  
- **Timestamp Properties**: Use "At" to indicate timestamp properties.
  - 🔍 **Example**: `createdAt`, `updatedAt`
  
- **Soft Deletes**: Use `deletedAt` to indicate soft delete timestamp properties.
  - 🔍 **Example**: `deletedAt`

- **Foreign Key Properties**: For foreign keys, use a combination of the related entity name followed by the name of the primary identifier of that entity.
  - 🔍 **Example**: `addressUuid`

### ✅ Preferred Properties

- **UUIDs**: Always prefer using UUIDs as identifiers to ensure uniqueness and security.
  - 🔍 **Example**: `userUuid`

- **Timestamps**: Always include `createdAt` and `updatedAt` timestamp properties to track entity lifecycle events.
  - 🔍 **Example**: `createdAt`, `updatedAt`

### 🚫 Prohibited Practices

- **Ambiguous Names**: Avoid using ambiguous or generic names for properties which do not clearly indicate their purpose or the data they hold.
  - **Example to Avoid**: `data`, `info`
  
- **Redundant Information**: Avoid including redundant information in property names.
  - **Example to Avoid**: `userUserName`, instead use `username`

---

## 🌱 Seeder Classes

Seeder classes are crucial in populating the database with initial data for testing or database initialization. Here are the conventions for seeder classes:

### 📁 File and Class Naming Conventions

- **Filename**: `<entity>.seeder.ts`
  - 🔍 **Example**: `user.seeder.ts`
  
- **Class Name**: Should be in PascalCase, followed by the word 'Seeder'.
  - 🔍 **Example**: `UserSeeder`, `AddressSeeder`

### 🛠 Main Methods

- **seedOne()**: This method seeds a single entity. 
  - **Usage**:

    ```typescript
    userSeeder.seedOne();
    ```

- **seedMany(number, options?)**: This method seeds multiple entities at once.
  - **Usage**:

    ```typescript
    userSeeder.seedMany(5);
    ```

## 🛡️ Custom Validators

To validate complex or specific business rules, the creation of custom validators with class-validator is encouraged. These custom validators enhance the validation process by allowing the enforcement of custom-defined rules on the data. Here are some conventions to follow when creating custom validators:

### 📄 File Naming Conventions

- **Filename**: Custom validators should be named clearly to indicate their functionality. The general pattern should be: `<functionality>.validator.ts`
  - 🔍 **Example**: `is-unique-username.validator.ts`, `is-valid-date.validator.ts`

### 🏷️ Class Naming Conventions

- **Class Name**: The class name should be descriptive and follow the PascalCase naming convention. It should ideally start with the "Is" prefix followed by the condition it's validating.
  - 🔍 **Example**: `IsUniqueUsername`, `IsValidDate`

### 🚧 Structure

- **Decorator Naming**: The custom validator should be usable as a decorator. The decorator name should clearly indicate the validation it performs and should be in camelCase.
  - 🔍 **Example**: `@isUniqueUsername`, `@isValidDate`

- **Error Messages**: Error messages should be user-friendly and adequately describe the validation error.
  - 🔍 **Example**: `'The username has already been taken.'`, `'The date format is not valid.'`

### 🛠️ Implementation

A custom validator class should implement the `ValidatorConstraintInterface` and define the `validate` and `defaultMessage` methods.

### 🌟 Example Implementation

```typescript
import { ValidatorConstraint, ValidatorConstraintInterface, ValidationArguments } from 'class-validator';

@ValidatorConstraint({ name: 'isUniqueUsername', async: false })
export class IsUniqueUsername implements ValidatorConstraintInterface {

    validate(username: any, args: ValidationArguments) {
        // Custom validation logic
        return true; // return false if the validation fails
    }

    defaultMessage(args: ValidationArguments) {
        return 'The username has already been taken.';
    }
}
```
---

## 🚀 Migrations

Migrations play a vital role in tracking and managing changes to the database schema. Here are the modified conventions to follow when creating or modifying migration files in the project:

### 📁 File Naming Conventions

Migration files should be named clearly to indicate the changes they introduce. Here are a few scenarios and how the naming could be approached:

1. **Creating an Entity**
   - Format: `<timestamp>Create<Entity>.ts`
   - Example: `1632394740324CreateUser.ts`

2. **Updating One or Multiple Properties of an Entity**
   - Format: `<timestamp>Update<Entity><PropertyDetails>.ts`
   - Example: `1632394740324UpdateUserAddDateOfBirth.ts`
   - Example: `1632394740324UpdateUserRemoveUsername.ts`

3. **Deleting an Entity**
   - Format: `<timestamp>Delete<Entity>.ts`
   - Example: `1632394740324DeleteUser.ts`

#### 🚫 Not Set in Stone

The naming conventions outlined above are guidelines to help maintain consistency. However, these are not set in stone; feel free to craft names that are descriptive yet concise to ensure clarity without resulting in overly complex names.

### 📂 File Structure

Structure your changes logically inside a migration file, and use comments to explain complex alterations. Each file should generally include:

- A vivid description of the migration at the top of the file.
- The `up` method to enact the migration.
- The `down` method to revert the migration.

### 🔎 Additional Guidelines

- **Single Responsibility**: Aim to have each migration file handle a single concern, keeping changes isolated and comprehensible.
- **Testing**: It's essential to rigorously test migration files to ensure they implement and reverse changes correctly without introducing bugs.

### 📝 Example File Structure

```typescript
import {MigrationInterface, QueryRunner} from "typeorm";

export class CreateUser1632394740324 implements MigrationInterface {

    public async up(queryRunner: QueryRunner): Promise<void> {
        // Up migration logic
    }

    public async down(queryRunner: QueryRunner): Promise<void> {
        // Down migration logic
    }
}

```
---

## 🌐 Query Parameters

Query parameters are utilized to filter, sort, and perform searches on the dataset in various API endpoints. These parameters are categorized into 'sort', 'like', and 'match'. Here are the conventions to follow when implementing and using these query parameters:

### ⬆️⬇️ Sort

The 'sort' parameter is used to order the results based on specified properties and a direction ('ASC' for ascending and 'DESC' for descending). Here is how it should be used:

- Parameter Name: `sort`
- Structure: `{<property>:(ASC|DESC)}`
- Multiple sorting can be applied using comma separation inside the object.
- Example: `sort={createdOn:DESC,username:ASC}`

### 🎯 Match

The 'match' parameter allows filtering results based on an exact match for specified properties. It can match multiple values for a single property. When trying to match properties of a relation, it should always first mention the relation's name followed by the property, with 'Uuid' used to address the primary key of the relation.

- Parameter Name: `match`
- Structure: `{<property>:[value1,value2,...]}`
- Property names should be singular, even when matching multiple values.
- Example: `match={username:[john,doe]}`
- Example (Relation): `match={petUuid:[123,456],petName:[fluffy,spot]}`

### 🔄 Like

The 'like' parameter facilitates searching for partial matches in the dataset, based on a single string.

- Parameter Name: `like`
- Structure: `{<property>:<partial-string>}`
- Example: `like={username:jo}`
- Example (Relation): `like={petName:fluf}`

---

## 🛠 General Conventions

This section outlines the general conventions that should be followed across different aspects of the codebase including functions, enums, and environment variables.

### 🎛 Functions

- **Visibility**: The visibility of functions (public, private, protected, etc.) should always be explicitly defined.
- **Examples**:
  ```typescript
  public getUser() { ... }
  private validateInput(input: any) { ... }
  protected formatResponse(response: any) { ... }
  ```

### 🚀 Enums

Enums are used to define a set of named constants. The following conventions should be adhered to when working with enums:

- **Naming Convention**: Enums should be in camelCase and should end with the word "Enum". 
- **Key**: The keys should be in UPPER_SNAKE_CASE.
- **Value**: The values should be in lower_snake_case.
- **File Name**: The file name should follow kebab-case, similar to other files, and end with `.enum.ts`.
  
  #### Examples:
  - **File Name**: `user-status.enum.ts`
  
  - **Enum Definition**:
    ```typescript
    export enum UserStatus {
      ACTIVE_STATUS = 'active_status',
      INACTIVE_STATUS = 'inactive_status',
    }
    ```

### ⚙️ Environment Variables

Environment variables are used to manage configurable values in the application. They should follow the following conventions:

- **Naming Convention**: Environment variables should be in UPPER_SNAKE_CASE.
- **Structure**: Start with the name of the service or external entity, followed by the specific attribute or detail.

  #### Examples:
  - `DATABASE_URL`
  - `EXTERNALSERVICE_AUTH_SECRET`
  - `APP_PORT`


---

## 📚 References & Further Reading

In your journey to mastering naming conventions in NestJS, you may find the following resources beneficial:

1. 📖 **[NestJS Documentation](https://docs.nestjs.com/)**
   - The official documentation provides a comprehensive guide to various aspects of NestJS, including best practices for naming conventions.
   
2. 📚 **[Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)**
   - This book by Robert C. Martin offers insights into writing clean, maintainable, and scalable code, which includes adhering to effective naming conventions.
   
3. 💻 **[TypeScript Naming Conventions](https://basarat.gitbook.io/typescript/styleguide#naming)**
   - A guide that outlines the naming conventions commonly used in TypeScript projects, which can be applied to NestJS projects as well.

4. 🎓 **[NestJS Best Practices](https://wanago.io/courses/nest-js-best-practices/)**
   - A course that delves deep into the best practices of building applications with NestJS, including naming conventions.

5. 🌐 **Community Forums and Blogs**
   - Engaging with the community through forums and blogs can provide real-world insights and tips on adhering to naming conventions in NestJS projects. Platforms like [Stack Overflow](https://stackoverflow.com/questions/tagged/nestjs) and [NestJS GitHub Discussions](https://github.com/nestjs/nest/discussions) can be good starting points.

Remember, the key to mastering naming conventions lies in consistent practice and learning from the experiences of seasoned developers in the community. Happy coding!
