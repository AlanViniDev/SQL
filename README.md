#create database cadastros;
#use cadastros;
#create table produtos (id_produto int not null,produto_id int not null auto_increment,
#nome varchar(255),marca varchar(255),preco double(4,3), primary key(produto_id));
#create table categorias (produto_id int not null auto_increment, nome varchar(255), primary key(produto_id));
#drop table produtos;
#drop table categorias;
#alter table produtos add constraint categoria_fk foreign key (produto_id) references categorias(produto_id);
#show tables;
#describe categorias;
#describe produtos;
#insert into produtos(id_produto,produto_id,nome,marca,preco)values(1,1,'macarrao','saborele',2.1);
#insert into categorias (nome)values('massas');
#select * from categorias;
#select * from produtos;
SELECT prod.id_produto,prod.nome,prod.marca,prod.preco,cate.categoria FROM produtos prod INNER JOIN categorias cate on prod.id_produto = cate.produto_id;
#ALTER TABLE categorias drop column nome;
#ALTER TABLE categorias ADD COLUMN categoria varchar(255);
#UPDATE categorias SET categoria = 'massas' where produto_id = 1;
