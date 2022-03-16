# &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```FreshTech App```

###### Creation of database - FreshTech

####  ```create database FreshTech;```

###### Using database - FreshTech

#### ```use FreshTech;```

###### Creation of table 1 - 'users'

#### ```create table users(user_id tinyint primary key auto_increment,user_name varchar(20) not null check(length(user_name)>=3),user_mailId varchar(50) not null unique check(user_mailId like("_%@gmail.com")),user_password varchar(15) not null check(validate_password_strength(user_password)=100),join_date date not null);```

#### ```desc users;```

![describe users](https://user-images.githubusercontent.com/93571047/158520349-7827c435-6bd9-4956-93a6-c7edebde1bfc.png)

###### Insertion of Records into 'users' table

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Chitra Muthukumaran","chitram@gmail.com","Chitra@1234","2007/09/24");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Revathi Iyer","revathiiyer@gmail.com","Revathi@1234","1998/12/12");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Prasanna Bharathi","prasannabharathi@gmail.com","Prasanna@1234","2010/12/12");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Shyam","shanmugaanantharaman@gmail.com","Shyam@1234","2010/12/12");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Deepak Panneerselvam","deepak@gmail.com","Deepak@1234","2021/10/04");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Kasi Antony","kasi@gmail.com","Kasi@1234","2021-10-04"),("Keerthana","keerthana@gmail.com","Keerthi@1234","2021-10-04"),("Meenu Sowjanya","msowjanyac@gmail.com","Meenu@1234","2021-10-04");```

#### ```insert into users(user_name,user_mailId,user_password,join_date) values("Pavan Raaj","pavan@gmail.com","Pavan@1234","2021-10-04"),("Venkatakkrishnan","venkat@gmail.com","Venki@1234","2021-10-04"),("Vaishnavi","vaishnavi@gmail.com","Vaishnavi@1234","2021-10-04");```

###### Fetching the data in 'users' table

#### ```select * from users;```


| user_id | user_name            | user_mailId                    | user_password  | join_date  |
|:--:|:--:
|       1 | Chitra Muthukumaran  | chitram@gmail.com              | Chitra@1234    | 2007-09-24 |
|       2 | Revathi Iyer         | revathiiyer@gmail.com          | Revathi@1234   | 1998-12-12 |
|       3 | Prasanna Bharathi    | prasannabharathi@gmail.com     | Prasanna@1234  | 2010-12-12 |
|       4 | Shyam                | shanmugaanantharaman@gmail.com | Shyam@1234     | 2010-12-12 |
|       5 | Deepak Panneerselvam | deepak@gmail.com               | Deepak@1234    | 2021-10-04 |
|       6 | Kasi Antony          | kasi@gmail.com                 | Kasi@1234      | 2021-10-04 |
|       7 | Keerthana            | keerthana@gmail.com            | Keerthi@1234   | 2021-10-04 |
|       8 | Meenu Sowjanya       | msowjanyac@gmail.com           | Meenu@1234     | 2021-10-04 |
|       9 | Pavan Raaj           | pavan@gmail.com                | Pavan@1234     | 2021-10-04 |
|      10 | Venkatakkrishnan     | venkat@gmail.com               | Venki@1234     | 2021-10-04 |
|      11 | Vaishnavi            | vaishnavi@gmail.com            | Vaishnavi@1234 | 2021-10-04 |



