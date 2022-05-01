# PROYECTO-FINAL-JOSE-FELIZ
PROYECTO FINAL DE BASE DE DATOS / JOSE FRANCISCO FELIZ GOMEZ / 20-SIIT-1-003

create database JFSOFTECH
use JFSOFTECH

                 /***EMPRESA DE SOFTWARE***/
/***JOSE FRANCISCO FELIZ GOMEZ / 20-SIIT-1-003 / Seccion: 0541 ***/

 create table cliente1 (
  id_cliente int identity(1,1) primary key, 
  nombre varchar(30) not null,
  Telefono varchar (30),
  calle varchar(30),
  ciudad varchar(20),
  pais varchar(20),
 );


 insert into cliente1
  values ('Manuel Feliz','809123456','Sarasota', 'Santo Domingo','Republica Dominicana');
  insert into cliente1
  values ('Adamarys Silva','8092135896', 'Churchill','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Juan Garcia','8293546969', 'Lincoln','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Luis Perez','8495898985', '27 de Febrero','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Ines Gomez','2498574587', 'Independencia','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Adderly Guerrero','8294566365', 'Kenedy','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Carlos Rivera','8297855487', 'Jose Contreras','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Betania Ramos','8095486873', 'Abraham Lincoln','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Fernando Salas','8493215689', 'Independencia','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('German Rojas','8095462536', 'Churchill','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Ricardo Jara','8095633214', 'Defilló','Santo Domingo','Republica Dominicana');
 insert into cliente1
  values ('Joaquin Robles','8095879896', 'Privada','Santo Domingo','Republica Dominicana');



  create table producto (
  id_producto int identity(1,1) primary key, 
  precio varchar (30),
  descripcion varchar (30) not null,
  );

insert into producto
  values ('001','50000','Sistema Automatizado');
insert into producto
  values ('002','50000','Sistema Automatizado');
insert into producto
  values ('003','50000','Sistema Automatizado');
insert into producto
  values ('004','50000','Sistema Automatizado');
insert into producto
  values ('005','50000','Sistema Automatizado');
insert into producto
  values ('006','50000','Sistema Automatizado');
  insert into producto
  values ('007','50000','Sistema Automatizado');
 insert into producto
  values ('008','50000','Sistema Automatizado');
insert into producto
  values ('009','50000','Sistema Automatizado');
insert into producto
  values ('0010','50000','Sistema Automatizado');
insert into producto
  values ('0011','50000','Sistema Automatizado');



  create table factura3 (
  id_factura int identity(1,1) primary key, 
  id_cliente int foreign key (id_cliente) references cliente(id_cliente),
  Total_producto varchar (30),
  fecha  varchar (30) not null,
  direccion  varchar (30),
  ciudad  varchar (30),
  );

  insert into factura3
  values ('001','50000','02/01/2022','Churchill 202','Santo Domingo');
 insert into factura3
  values ('001','50000','02/01/2022','Churchill 202','Santo Domingo');
insert into factura3
  values ('002','50000','03/02/2022','Lincol 24','Santo Domingo');
insert into factura3
  values ('003','50000','04/03/2022','Republica de Colombia 12','Santo Domingo');
insert into factura3
  values ('004','50000','05/05/2022','Independencia 01','Santo Domingo');
insert into factura3
  values ('005','50000','06/05/2022','Kenedy 1215','Santo Domingo');
insert into factura3
  values ('006','50000','07/03/2022','Lopez de Vega 203','Santo Domingo');
insert into factura3
  values ('007','50000','08/10/2022','Anacaona 105','Santo Domingo');
insert into factura3
  values ('008','50000','09/11/2022','Sarasota 10','Santo Domingo');
insert into factura3
  values ('009','50000','10/12/2022','Lincoln 102','Santo Domingo');
insert into factura3
  values ('0010','50000','11/12/2022','27 de Febrero 25','Santo Domingo');
insert into factura3
  values ('0011','50000','12/01/2022','Kenedy 305','Santo Domingo');


  create table detalle_logistica_venta12 (
  id_detalle_logistica_venta  int identity(1,1) primary key, 
  id_producto varchar (30)not null,
  id_factura int foreign key (id_factura) references factura(id_factura),
  id_cliente varchar (30),
  numero_orden varchar (30),
  cantidad  varchar (30) not null,
  producto  varchar (30),
 );

  
    insert into detalle_logistica_venta12
  values ('123','10','1000','101','5','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('456','20','2000','102','2','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('789','30','3000','103','1','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('357','40','4000','104','2','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('159','50','5000','105','2','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('486','60','6000','106','6','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('426','70','7000','107','3','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('497','80','8000','108','7','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('356','90','9000','109','5','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('453','100','11000','110','5','Sistema Automatizado');
   insert into detalle_logistica_venta12
  values ('173','110','12000','111','3','Sistema Automatizado');

  
  create table contrato_mantenimiento1 (
  id_contrato_mantenimiento int identity(1,1) primary key,
  fecha_desde varchar (30) not null,
  fecha_hasta varchar (30) not null,
  pago_total varchar (30) not null,
  );

  insert into contrato_mantenimiento1
  values ('01/02/2022','01/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('02/02/2022','02/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('03/02/2022','03/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('04/02/2022','04/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('05/02/2022','05/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('06/02/2022','06/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('07/02/2022','07/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('08/02/2022','08/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('09/02/2022','09/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('10/02/2022','10/08/2022','25000');
   insert into contrato_mantenimiento1
  values ('11/02/2022','11/08/2022','25000');

  select *from cliente1
  select *from producto
  select *from factura1
  select *from detalle_logistica_venta1
  select *from contrato_mantenimiento
 
