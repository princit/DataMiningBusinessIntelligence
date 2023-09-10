# SQL Basics
used for 

1-storing and 
2-managing data
RDBMS

It not case sensitive.

# Types of SQL Commands
• There are five types of SQL commands: DDL, DML,
DCL, TCL, and DQL.
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/f0a99f73-3001-46fd-9eb0-50d91e9edbaa)

  <table>
    <thead>
      <tr>
        <th>Index</th>
        <th>View</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>create Unique index index_name on table_name</td>
            <td>create View Detail view as select name,address from stu_detail</td>
        </tr>
        <tr>
            <td>Drop index index_name</td>
            <td>Drop view view_Name</td>
        </tr>

    </tbody>
  </table>
  
  # sub-query 
outer query ->main query 
inner query ->sub query 
unique/not exist/ exist/not in/some/all

insert into Employfrom`ee_BMP
select * from Employee
where ID IN (select ID from Employee)

# SQL Clause
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/07970c59-7753-4e7f-badc-9c6a16be64a9)

# Join


  <table>
    <thead>
      <tr>
        <th>Inner Join</th>
        <th>Left Join</th>
        <th>Right Join</th>
        <th>Full Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>matching Value in both table</td>
            <td>return All value from left table only matching value in right table </td>
            <td>return All value from right table only matching value in left table </td>
            <td>return combination of right and left outer join ,Put null where match not found</td>
        </tr>
    </tbody>
  </table>
 
  # Operation
  <table>
    <thead>
      <tr>
        <th>Union</th>
        <th>Intersection</th>
        <th>Minus</th>
        <th>Except</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>Eliminate duplicate row</td>
            <td>common row form both </td>
            <td>Present first but absent in second </td>
            <td>return combination of right and left outer join ,Put null where match not found</td>
        </tr>
        <tr>
            <td>select * from first union select * from second</td>
            <td>select * from first intersection select * from second</td>
            <td>select * from first minus select * from second</td>
            <td>select * from first except select * from second</td>
        </tr>
    </tbody>
  </table>


mysql -u yourdbuser -p Yourdbbase

  # Cartisean Product
  <table>
    <thead>
      <tr>
        <th>Where</th>
        <th>Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>select * from instructor,teacher where instructor.ID = teacher.ID</td>
            <td>select * from Epmployee inner join project on project.Emp_ID = Employee.Emp_ID </td>
        </tr>
    </tbody>
  </table>

select name from instructor where salary between 90 and 100

  # Tuple Comparision

  select name,course_id from intructor,teacher where (instructor.ID,dept_name) = (Teacher.ID,"Bilogy")

  insert into table1 select * from table1

  # Updates with Scalar Subqueries
  <table>
    <thead>
      <tr>
        <th>Where</th>
        <th>Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>update instructor set salary = case when salary <= 100 then salary*1.05 else salary*103 end</td>
            <td>update student s set tot_cred = (select sum(credits) from takes,course where take.cource_id=cource.course _id and s.ID = take.ID and take.grade<'F' and takes.grade is not null) </td>
        </tr>
    </tbody>
  </table>
