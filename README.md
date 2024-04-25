CREATE TABLE Produto 
( 
 ID do Produto INT,  
 Nome do produto VARCHAR(n),  
 Preço (u) INT,  
 Estoque INT,  
 ID do Fornecedor INT,  
); 

CREATE TABLE Vendedor 
( 
 ID do vendedor INT PRIMARY KEY,  
 Nome INT,  
 Contato INT,  
 E-mail INT,  
 CPF INT,  
); 

CREATE TABLE Fornecedor 
( 
 ID do Fornecedor INT PRIMARY KEY,  
 CNPJ VARCHAR(n),  
 Nome da Empresa VARCHAR(n),  
); 

CREATE TABLE Vendas 
( 
 ID da transação INT PRIMARY KEY,  
 Valor INT DEFAULT 'Texto',  
 Data DATE,  
 ID do cliente INT,  
 ID do vendedor INT,  
); 

CREATE TABLE Venda do produto 
( 
 ID do produto INT,  
 ID da transação INT,  
); 

CREATE TABLE Cliente 
( 
 ID do cliente INT PRIMARY KEY,  
 Nome INT,  
 CPF INT,  
 Contato INT,  
); 

ALTER TABLE Produto ADD FOREIGN KEY(ID do Fornecedor) REFERENCES Fornecedor (ID do Fornecedor)
ALTER TABLE Vendedor ADD FOREIGN KEY(CPF) REFERENCES Produto (CPF)
ALTER TABLE Vendas ADD FOREIGN KEY(ID do cliente) REFERENCES Cliente (ID do cliente)
ALTER TABLE Vendas ADD FOREIGN KEY(ID do vendedor) REFERENCES Vendedor (ID do vendedor)
ALTER TABLE Venda do produto ADD FOREIGN KEY(ID do produto) REFERENCES Produto (ID do produto)
ALTER TABLE Venda do produto ADD FOREIGN KEY(ID da transação) REFERENCES Vendas (ID da transação)
