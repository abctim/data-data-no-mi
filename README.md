# data-data-no-mi

Welcome to the Data Data no Mi project! This project is a fun way to explore and learn about Hibernate, PostgreSQL, entity relationships, primary and foreign keys, fetching strategies, and the usage of ElementCollection with an enum using the popular manga and anime series, One Piece.

## Project Description

The Data Data no Mi project is a One Piece Episode Management System that demonstrates the use of various database concepts and technologies. The project utilizes Hibernate as the Object-Relational Mapping (ORM) tool to interact with a PostgreSQL database. It showcases the implementation of entity relationships, primary and foreign keys, optimized fetching strategies, and the usage of ElementCollection with an enum.

The project consists of the following entities:

1. Episode
  - id (Long, Primary Key)
  - title (String)
  - number (Integer)
  - airDate (Date)
  - synopsis (String)
  - arc (Many-to-One Relation to Arc)

2. Arc
  - id (Long, Primary Key)
  - name (String)
  - description (String)
  - episodes (One-to-Many Relation to Episode)

3. Character
  - id (Long, Primary Key)
  - firstName (String)
  - lastName (String)
  - role (String)
  - devilFruit (String)
  - appearances (Many-to-Many Relation to Episode)
  - haki (ElementCollection of Haki enum)

4. User
  - id (Long, Primary Key)
  - username (String)
  - email (String)
  - favoriteCharacters (Many-to-Many Relation to Character)
  - watchedEpisodes (Many-to-Many Relation to Episode)

The `Character` entity includes an `ElementCollection` of the `Haki` enum, which represents the types of Haki (a special power in the One Piece universe) that a character possesses. The `Haki` enum can have values such as `OBSERVATION`, `ARMAMENT`, and `CONQUEROR`.

## Technologies Used

- Java
- Hibernate
- PostgreSQL
