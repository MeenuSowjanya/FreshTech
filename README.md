# &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```FreshTech App```

###### Creation of database - FreshTech

 ```create database FreshTech;```

###### Using database - FreshTech

```use FreshTech;``` 

###### Creation of table 1 - 'users'

```create table users(user_id tinyint primary key auto_increment,user_name varchar(20) not null check(length(user_name)>=3),user_mailId varchar(50) not null unique check(user_mailId like("_%@gmail.com")),user_password varchar(15) not null check(validate_password_strength(user_password)=100),join_date date not null);```
```desc users;```

![describe users](https://user-images.githubusercontent.com/93571047/158520349-7827c435-6bd9-4956-93a6-c7edebde1bfc.png)

###### Insertion of Records into 'users' table
<b>
 
 ```insert into users(user_name,user_mailId,user_password,join_date) values("Chitra Muthukumaran","chitram@gmail.com","Chitra@1234","2007/09/24");```

 ```insert into users(user_name,user_mailId,user_password,join_date) values("Revathi Iyer","revathiiyer@gmail.com","Revathi@1234","1998/12/12");```
 
 ```insert into users(user_name,user_mailId,user_password,join_date) values("Prasanna Bharathi","prasannabharathi@gmail.com","Prasanna@1234","2010/12/12");```

 ```insert into users(user_name,user_mailId,user_password,join_date) values("Shyam","shanmugaanantharaman@gmail.com","Shyam@1234","2010/12/12");```

 ```insert into users(user_name,user_mailId,user_password,join_date) values("Deepak Panneerselvam","deepak@gmail.com","Deepak@1234","2021/10/04");```

 ```insert into users(user_name,user_mailId,user_password,join_date) values("Kasi Antony","kasi@gmail.com","Kasi@1234","2021-10-04"),("Keerthana","keerthana@gmail.com","Keerthi@1234","2021-10-04"),("Meenu Sowjanya","msowjanyac@gmail.com","Meenu@1234","2021-10-04");```

 ```insert into users(user_name,user_mailId,user_password,join_date) values("Pavan Raaj","pavan@gmail.com","Pavan@1234","2021-10-04"),("Venkatakkrishnan","venkat@gmail.com","Venki@1234","2021-10-04"),("Vaishnavi","vaishnavi@gmail.com","Vaishnavi@1234","2021-10-04");``` </b>

###### Fetching the data in 'users' table

<b> ```select * from users;```</b>

![select * from users](https://user-images.githubusercontent.com/93571047/158520738-970c5a7c-6101-4782-9fff-21187a64e67f.png)

###### Creation of table 2 - 'user_contacts'

<b> ```create table user_contacts(user_id tinyint not null,user_phoneNo bigint check(user_phoneNo like("__________"),foreign key(user_id) references users(user_id));```</b>

``` desc user_contacts; ```

![describe user_contacts](https://user-images.githubusercontent.com/93571047/158522419-65fd18e1-dcf3-4d4c-be52-2f39305027e1.png)

###### Insertion of records into 'user_contacts' table

<b> ```insert into user_contacts values(1,9442972004);``` 

```insert into user_contacts values(1,9842448168),(2,7402066305),(3,7448354949),(4,7989899993),(4,9087654321),(4,9890988976),(5,9678876901),(6,9345678890),(7,9012345678),(8,9876543210),(9,9654321098),(10,9876900984),(11,7658904554);``` </b>

###### Fetching the data in 'user_contacts' table

![select * from user_contacts](https://user-images.githubusercontent.com/93571047/158523061-c03243c7-9af9-483d-8ca1-1e62d1cd24cb.png)

###### creation of table 3 - 'user_address'

<b>
 ``` create table user_address(user_Id tinyint unique,door_no varchar(10) not null,street varchar(30),city varchar(25) not null,state varchar(25) not null,`pin-code` int check(`pin-code` like("______")),foreign key(user_Id) references users(user_id)) ; ```
 
 ``` desc user_address; ```
 
 ![describe user_address](https://user-images.githubusercontent.com/93571047/158528840-d9e9962d-fdbe-43d1-b17f-e0b241e77efb.png)
 
 </b>
 
 ###### Insertion of records into 'user_address' table
 
 <b>
 
 ```insert into user_address values(1,"L-84","Police Colony","Annanagar (PO)","Trichy",620026);```
 
 ```insert into user_address values(2,"L-84","Police Colony","Annanagar (PO)","Trichy",620026);```
 
 ```insert into user_address values(3,"M-84","Police Colony","Annanagar (PO)","Chennai",620001);```
 
 ```insert into user_address values(4,"M-84","Police Colony","Annanagar (PO)","Chennai",620001),(5,"M-84","Arihant Nagar","Koyambedu (PO)","Chennai",620001),(6,"L-83","Perungudi","Kandanchavadi (PO)","Kanchipuram",620001),(7,"M-84","Police Colony","Kothagiri (PO)","Ooty",620010),(8,"M-84","Duraiappa Colony","Kayalpatinam(PO)","Thootukudi",620007),(9,"G-84","Collector Office Street","Avinasi (PO)","Tirupur",620009),(10,"P-84","Saibaba Colony","Boothamangalam (PO)","Coimbatore",620067),(11,"O-84","Police Colony","Perumangalam (PO)","Pondichery",620020);```
 
 </b>
 
 ###### Fetching the data in 'user_address' table
 
 ![select * from user_address](https://user-images.githubusercontent.com/93571047/158529465-b14406e4-1506-4848-8b0b-adbab59892c7.png)
