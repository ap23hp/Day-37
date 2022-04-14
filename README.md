# Day-37


> Task Table

create table task (task_id int auto_increment, task_name varchar(255) , Days_For_Completion int ,  Batch  varchar(255) not null default ('repeater'), primary key(task_id) , foreign key (task_id) references student(id) );

insert into task ( task_name  , Days_For_Completion ,  Batch) values ('Crud task', '7' , 'Batch_1');
insert into task ( task_name  , Days_For_Completion ,  Batch) values ('Formik', '5' , 'Batch_2');
insert into task ( task_name  , Days_For_Completion ,  Batch) values ('router', '2' , 'Batch_3');
insert into task ( task_name  , Days_For_Completion,Batch) values ('display items ', '1', 'repeater');
drop table task;
select * from task;


>Student table


create table studentCollection(
studentID int(10)  primary key,
studentName varchar(50) not null,
email varchar(50) not null,
courseID int(10)
)



insert into studentCollection value(1205,"john","jogn@gmail.com",123458);
insert into studentCollection value(1206,"Michel","mmm@gmail.com",123457);
insert into studenCollection value(1207 ,"harry","hhh@gmail.com",123456);
insert into studenCollection value(1208,"felix","ghf@yahoo.com",123455);
insert into studenCollection value(1209,"pinto","refr@gmail.com",123454);
insert into studentCollection  value(1210,"yettenia","tre@gmail.com",123453);


select * from student;




>Mentor table


create table mentor ( mentor_Id int auto_increment , mentor_name varChar(255) unique , specilization varchar(255) , primary Key (mentor_name ) , foreign key(mentor_id) references batch(batch_id)) ;


insert into mentor ( mentor_name ,specilization) values ('Mentor_1', 'FSD');
insert into mentor ( mentor_name ,specilization) values ('Mentor_2', 'React');
insert into mentor ( mentor_name ,specilization) values ('Mentor_3', 'JAva');
insert into mentor ( mentor_name ,specilization) values ('Mentor_4', 'MongoDB');
insert into mentor ( mentor_name ,specilization) values ('Mentor_5', 'HTML');
insert into mentor ( mentor_name ,specilization) values ('Mentor_6', 'Data Science');
insert into mentor ( mentor_name ,specilization) values ('Mentor_7', 'AI');
insert into mentor ( mentor_name ,specilization) values ('Mentor_8', 'JS');

drop table mentor ;
select * from mentor ;


> Batch table

create table Batch ( batch_id int auto_increment , course varchar(255), langauge enum('Hindi' , 'English') default 'English' , student_Id int  unique, primary key (batch_id) , foreign key (batch_id) references  student(id) ) ;

insert into batch(course, student_Id ) values ( 'FSD' ,1);
insert into batch(course, langauge, student_Id ) values ('React' , 'English', 2);
insert into batch(course, langauge, student_Id ) values ('Java' , 'Hindi', 3);
insert into batch(course, student_Id ) values ('MongoDB' , 9);
insert into batch(course, langauge, student_Id ) values ('HTML' , 'Hindi', 5);
insert into batch(course, langauge, student_Id ) values ('JS' , 'English', 6);
insert into batch(course, student_Id ) values ('Data Science' , 7);
insert into batch(course, student_Id ) values ('AI' , 8);
select * from Batch;
drop table Batch;




