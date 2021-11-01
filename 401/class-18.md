# Web App Security

## Many to many relationships:

![ManyToMany](https://www.baeldung.com/wp-content/uploads/2017/09/New.png)

In this scenario, any given employee can be assigned to multiple projects and a project may have multiple employees working for it, leading to a many-to-many association between the two.

We have an employee table with employee_id as its primary key and a project table with project_id as its primary key. A join table employee_project is required here to connect both sides.


### Database Setup

    CREATE TABLE `employee` (
    `employee_id` int(11) NOT NULL AUTO_INCREMENT,
    `first_name` varchar(50) DEFAULT NULL,
    `last_name` varchar(50) DEFAULT NULL,
    PRIMARY KEY (`employee_id`)
    ) ENGINE=InnoDB AUTO_INCREMENT=17 DEFAULT CHARSET=utf8;

    CREATE TABLE `project` (
    `project_id` int(11) NOT NULL AUTO_INCREMENT,
    `title` varchar(50) DEFAULT NULL,
    PRIMARY KEY (`project_id`)
    ) ENGINE=InnoDB AUTO_INCREMENT=18 DEFAULT CHARSET=utf8;

    CREATE TABLE `employee_project` (
    `employee_id` int(11) NOT NULL,
    `project_id` int(11) NOT NULL,
    PRIMARY KEY (`employee_id`,`project_id`),
    KEY `project_id` (`project_id`),
    CONSTRAINT `employee_project_ibfk_1` 
    FOREIGN KEY (`employee_id`) REFERENCES `employee` (`employee_id`),
    CONSTRAINT `employee_project_ibfk_2` 
    FOREIGN KEY (`project_id`) REFERENCES `project` (`project_id`)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8;


### The Model Classes
    @Entity
    @Table(name = "Employee")
    public class Employee { 
        // ...
    
        @ManyToMany(cascade = { CascadeType.ALL })
        @JoinTable(
            name = "Employee_Project", 
            joinColumns = { @JoinColumn(name = "employee_id") }, 
            inverseJoinColumns = { @JoinColumn(name = "project_id") }
        )
        Set<Project> projects = new HashSet<>();
    
        // standard constructor/getters/setters
    }

    @Entity
    @Table(name = "Employee")
    public class Employee { 
        // ...
    
        @ManyToMany(cascade = { CascadeType.ALL })
        @JoinTable(
            name = "Employee_Project", 
            joinColumns = { @JoinColumn(name = "employee_id") }, 
            inverseJoinColumns = { @JoinColumn(name = "project_id") }
        )
        Set<Project> projects = new HashSet<>();
    
        // standard constructor/getters/setters
    }


## Security: a humorous overview

> Thinking about security is like thinking about where to ride your motorcycle: the safe places are no fun, and the fun places are not safe. I shall ride wherever my spirit takes me, and I shall find my Gigantic Martian Insect Party, and I will, uh, probably be rent asunder by huge cryptozoological mandibles, but I will die like Thomas Jefferson: free, defiant, and without a security label.

This is quoted from James Mickens, a researcher in the Distributed Systems group at Microsoft's Redmond lab.

So security attacks will depend on who is hacking, so if it was just a guy who wants to trick some people to get some money. But if it was a Mossad type of attack, then all you can do is watching them do it. They will get your data and everything about you no matter what you do. 

Also, he mentions making good security while coding, as it is so boring and requires a lot of work, so evetually it will be so hard to get it all done in big applications. And that is why James mentioned that the secure path is so boring, as it requires alot of extra hard work in order to secure the data.


