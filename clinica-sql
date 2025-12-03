create database CLINICA;
create table SALA(
Cod_Sala int NOT NULL auto_increment,
Numero_Sala int NOT NULL,
Andar int NOT NULL,
unique (Numero_Sala),
unique (Andar),
primary key (Cod_Sala)
)
;
create table MEDICO(
Cod_Medico int NOT NULL auto_increment,
CRM varchar (15) NOT NULL, 
Nome varchar (40) NOT NULL,
Idade int,
Especialidade varchar (20) NOT NULL default 'Ortopedia',
CPF varchar (15) NOT NULL,
unique (CPF),
unique (CRM),
primary key (Cod_Medico)
);
create table PACIENTE(
Cod_Paciente int NOT NULL auto_increment,
RG varchar (15) NOT NULL,
Nome varchar (40) NOT NULL,
Data_Nascimento date,
Cidade varchar (30) default 'Itabuna',
Plano_Saude varchar (40) default 'SUS',
unique(RG),
primary key (Cod_Paciente)
);
create table FUNCIONARIO(
Cod_Funcionario int auto_increment,
Matricula varchar (15) NOT NULL,
Nome varchar (40) NOT NULL,
Data_Nascimento date,
Data_Admissao date,
Cargo varchar (40) default 'Assistente Médico',
Salario float default '510.00',
unique (Matricula),
primary key (Cod_Funcionario)
);
create table CONSULTA(
Cod_Consulta int NOT NULL auto_increment,
Cod_Med int,
Cod_Paci int,
Data_Horario date,
Cod_Medico int, 
foreign key(Cod_Med) references MEDICO(Cod_Medico),
foreign key(Cod_Paci) references PACIENTE(Cod_Paciente),
primary key (Cod_Consulta)
);
