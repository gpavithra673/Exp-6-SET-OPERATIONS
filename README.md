# Exp-6-SET-OPERATIONS
## AIM:
### To use set operations(union,union all,intersect,expect) in SQL.
## ALGORITHM:
### STEP 1: Create a sample table in SQL using CREATE TABLE syntax
### STEP 2: Insert all the values and Titles respectively using INSERT INTO syntax
### STEP 3: Now check whether all the rows are affected or not by fetching the table
### STEP 4: After checking, use SELECT for choosing the column name that we want and use FROM to choose the table
### STEP 5: Then use set operations UNION, UNION ALL, INTERSECT and EXPECT to implement set operation. If intersect or expect is not supported then use IN and NOT IN for replacement.
### STEP 6: After compiling and running the program, the results will be displayed.
## PROGRAM:
### table
```
create table A1(
  ID int,
  Name varchar(50)
);
insert into A1 (ID,Name)
values (1,'Sakthi');
insert into A1(ID,Name)
values (2,'Alisha');
insert into A1 (ID,Name)
values (3,'Amoli ');
insert into A1(ID,Name)
values (4,'Nehrika');
insert into A1 (ID,Name)
values (5,'Prisha');
insert into A1(ID,Name)
values (6,'Geetika');
insert into A1(ID,Name)
values (7,'Hiya');
insert into A1(ID,Name)
values (8,'Shrishti');
insert into A1 (ID,Name)
values (9,'Taara');
insert into A1(ID,Name)
values (10,'Zara');

create table B1(
  ID int,
  Name varchar(50)
);
insert into B1(ID,Name)
values (1,'Sakthi');
insert into B1(ID,Name)
values (2,'Chitrasen');
insert into B1 (ID,Name)
values (3,'Devayan');
insert into B1(ID,Name)
values (4,'Girinath ');
insert into B1 (ID,Name)
values (5,'Nakulesh');
insert into B1 (ID,Name)
values (6,'Sudharma');
insert into B1 (ID,Name)
values (7,'Vijayrathna');
insert into B1 (ID,Name)
values (8,'Amey');
insert into B1 (ID,Name)
values (9,'Bhavesh');
insert into B1 (ID,Name)
values (10,'Chirayu');
insert into B1 (ID,Name)
values (11,'Chirayu');
```
### UNION:
```
select Name from A1
union
select Name from B1
order by Name;
```
### UNION ALL:
```
select Name from A1
union all
select Name from B1
order by Name;
```
### INTERSECT:
```
select Name from A1
where A1.Name in (select Name from B1);
```
### EXPECT :
```
select Name from A1
where A1.Name not in (select Name from B1);
```
## OUTPUT:
### UNION:
![image](https://github.com/gpavithra673/Exp-6-SET-OPERATIONS/assets/93427264/ab43f943-7465-42f7-ade1-039a4f5e2380)
### UNION ALL:
![image](https://github.com/gpavithra673/Exp-6-SET-OPERATIONS/assets/93427264/1b911ce3-2ab8-41b7-9713-cbe6a24986bf)
### INTERSECT:
![image](https://github.com/gpavithra673/Exp-6-SET-OPERATIONS/assets/93427264/f56df3f5-e099-48ba-9c66-95c24a9a6b3d)
### EXPECT :
![image](https://github.com/gpavithra673/Exp-6-SET-OPERATIONS/assets/93427264/a1fe9674-e549-44c9-89f6-26ea8891cc0e)

## RESULT:
### Thus we have successfully obtained the required result using the above-given code.
