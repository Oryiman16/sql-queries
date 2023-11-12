# sql-queries

My first call Procedure

delimiter ##
   create procedure insert data (`S/N` tinyint, `First Name` varchar (15), `Last Name` varchar (15),
  `Sub Family`set ('Nevkaa', 'Orbunde', 'TorIkpa', 'Allam'), `Phone Number` bigint, DOB date,
  `State of origin` varchar (10), `Time of payment` time , Age TINYint, sex char (6),
 `Job Title` varchar (15), `shoe size` enum ('5', '10', '15', '20', '25', '30', '35', '40', '45', '50'),
 `shirt size` enum ('XS', 'S', 'M', 'L','XL'), Salary decimal (8,2), contribution real, residence varchar (25))
   begin  
   start transaction;
     insert into `extended family`
     values  (`S/N`,  `First Name`, `Last Name` ,
  `Sub Family` , `Phone Number` , DOB ,
  `State of origin`, `Time of payment` , Age , sex ,
 `Job Title`, `shoe size` ,
 `shirt size` , Salary , contribution, residence);
   
   commit;
   end##
   delimiter ;

   call insertdata(28, 'Dooshima', 'Nevkaa', 'Nevkaa', '447824685564', '1987-06-01', 'benue',
   '04:33:00', '36', 'female', 'lecturer', '40', 'm', '993452', '40000', 'nottingham');


