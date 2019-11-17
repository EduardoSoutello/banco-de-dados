create database ELEIÇÃO;
create table CARGO(
Cod_Cargo int auto_increment,
Nome_Cargo varchar (30) NOT NULL,
Salario float default '17000.00',
primary key (Cod_Cargo)
);
create table CANDIDATO(
Cod_Candidato int auto_increment,
Numero_Candidato int NOT NULL,
Cargo int NOT NULL,
Partido int NOT NULL,
foreign key (Cargo) references CARGO(Cod_Cargo),
foreign key (Partido) references PARTIDO(Cod_Partido),
unique (Numero_Candidato),
primary key (Cod_Candidato)
);
create table PARTIDO(
Cod_Partido int auto_increment,
Codigo_Partido int NOT NULL,
Sigla varchar (5) NOT NULL,
Nome varchar (40) NOT NULL,
Numero int,
unique (Codigo_Partido),
unique (Sigla),
primary key(Cod_Partido)
);
create table ELEITOR(
Cod_Eleitor int auto_increment,
Titulo_Eleitor varchar (30) NOT NULL,
Zona_Eleitorl varchar (5) NOT NULL,
Sessao_Eleitoral varchar (5) NOT NULL,
unique (TiTulo_Eleitor),
primary key(Cod_Eleitor)
);
create table VOTO (
Cod_Voto int auto_increment,
Titulo_Eleitor varchar (30) NOT NULL,
Numero_Candidato int NOT NULL,
foreign key (Titulo_Eleitor) references ELEITOR(Titulo_Eleitor),
foreign key (Numero_Candidato) references CANDIDATO(Numero_Candidato),
unique (Titulo_Eleitor),
primary key (Cod_Voto)
);

describe ELEITOR;
alter table VOTO add column Data_Voto date;
alter table  PARTIDO drop column Numeor;
alter table ELEITOR add column Data_Nascimento date;

