# Room


## Overview: Saving data with Room
The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

+ Compile-time verification of SQL queries.
+ Convenience annotations that minimize repetitive and error-prone boilerplate code.
+ Streamlined database migration paths.

**Primary components**
There are three major components in Room:

+ The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
+ Data entities that represent tables in your app's database.
+ Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.


## Defining entities in Room:

**Anatomy of an entity**

You define each Room entity as a class that is annotated with @Entity. A Room entity includes fields for each column in the corresponding table in the database, including one or more columns that comprise the primary key.

**Support full-text search**

If your app requires very quick access to database information through full-text search (FTS), have your entities backed by a virtual table that uses either the FTS3 or FTS4 SQLite extension module. To use this capability, available in Room 2.1.0 and higher, add the @Fts3 or @Fts4 annotation to a given entity


## Related entities in Room

**Define one-to-one relationships**

In order to query the list of users and corresponding libraries, you must first model the one-to-one relationship between the two entities. To do this, create a new data class where each instance holds an instance of the parent entity and the corresponding instance of the child entity.

        public class UserAndLibrary {
            @Embedded public User user;
            @Relation(
                parentColumn = "userId",
                entityColumn = "userOwnerId"
            )
            public Library library;
        }


## Accessing data with Room

#### Convenience methods

+ Insert

    @Dao
    public interface UserDao {
        @Insert(onConflict = OnConflictStrategy.REPLACE)
        public void insertUsers(User... users);

        @Insert
        public void insertBothUsers(User user1, User user2);

        @Insert
        public void insertUsersAndFriends(User user, List<User> friends);
    }

+ Update

        @Dao
        public interface UserDao {
            @Update
            public void updateUsers(User... users);
        }

*Room uses the primary key to match passed entity instances to rows in the database. If there is no row with the same primary key, Room makes no changes.*

+ Delete

        @Dao
        public interface UserDao {
            @Delete
            public void deleteUsers(User... users);
        }


#### Query methods

*Simple queries*

        @Query("SELECT * FROM user")
        public User[] loadAllUsers();



**resources:** 

*[https://developer.android.com/training/data-storage/room#java](https://developer.android.com/training/data-storage/room#java)*

*[https://developer.android.com/training/data-storage/room/defining-data](https://developer.android.com/training/data-storage/room/defining-data)*

*[https://developer.android.com/training/data-storage/room/relationships](https://developer.android.com/training/data-storage/room/relationships)*

*[https://developer.android.com/training/data-storage/room/accessing-data#java](https://developer.android.com/training/data-storage/room/accessing-data#java)*


