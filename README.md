# Spring Archetype With Generics

This repository contains a project that has a structure based on generic types to create an API very quickly based on empty classes.

----

### How to use it?
1. You must clone the project.
2. Add your connection parameters in the `application.properties` file.
3. After that we must create a series of classes for each entity for which we want to create a CRUD:
   - An entity and a DTO
   - A converter that extends `AbstractDTOConverter` (Implementing the missing methods) annotated with `@Service`
   - A repository that extends `JPARepository`, annotated with `@Repository` and leave it blank
   - A service that extends `AbstractCRUDService`, annotated with `@Service` and leave it blank
   - A controller that extends `AbstractController`, annotated with `@RestController` and `@RequestMapping(path = "/your/path")`. Just leave it blank too.
4. Run the project!


---

### What are the endpoints?

the routes will always be

`path:port/<path-controller>/<method-action>`

For an example entity called example, the endpoints would be as follows:
* **GET** localhost:8080/example/get/{id} - Get an example entity by id
* **GET** localhost:8080/example/get/all - Get all example entities
* **POST** localhost:8080/example/save - Save example entity from json body.
* **POST** localhost:8080/example/save/all - Save all example entities from json body.
* **PUT** localhost:8080/example/save - modify example entity from json body.
* **PUT** localhost:8080/example/save/all - modify all example entities from json body.
* **DELETE** localhost:8080/example/delete - remove example entity from json body.
* **DELETE** localhost:8080/example/delete/{id} - remove example entity by id
---

### Final notes

It's something I use a lot, so I hope it helps you too. Enjoy it!