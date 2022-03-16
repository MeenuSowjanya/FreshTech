# &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```FreshTech App```

###### Creation of database - FreshTech

####  ```create database FreshTech;```

###### Using database - FreshTech

#### ```use FreshTech;```

###### Creation of table 1 - 'users'

#### ```create table users(user_id tinyint primary key auto_increment,user_name varchar(20) not null check(length(user_name)>=3),user_mailId varchar(50) not null unique check(user_mailId like("_%@gmail.com")),user_password varchar(15) not null check(validate_password_strength(user_password)=100),join_date date not null);```

#### ```desc users;```


| Field         | Type        | Null | Key | Default | Extra          |
|:--:|:--:|:--:|:--:|:--:|:--:|
| user_id       | tinyint     | NO   | PRI | NULL    | auto_increment |
| user_name     | varchar(20) | NO   |     | NULL    |                |
| user_mailId   | varchar(50) | NO   | UNI | NULL    |                |
| user_password | varchar(15) | NO   |     | NULL    |                |
| join_date     | date        | NO   |     | NULL    |                |



