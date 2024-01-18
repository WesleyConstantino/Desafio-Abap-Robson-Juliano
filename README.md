# Desafio-Abap-Robson-Juliano
EF do Abap pleno Robson Juliano passada como desafio para para ser desenvolvida individualmente no grupo de estudos.

                                                                                                                                                                                                                                                                                   TABELAS – se11 
Criar nova tabela, elemento de dados e domínios, para cadastro de cliente, com a descrição “Cadastro de clientes”. Os campos da tabela deverão ser conforme abaixo: OK 
Campo  	type 	chave 
Nome do Cliente 	Char50 	X 
RG 	Char10 	X 
CPF 	Char10 	X 
Endereço 	Char100 	 
email 	Char40 	 
telefone 	Numc12 	 
 
Criar nova tabela, elemento de dados e domínios, para registro de vendo ao cliente, com a descrição “Cadastro de vendas”. Os campos da tabela deverão ser conforme abaixo: OK 
Campo  	type 	chave 
cód da venda 	Int 	x 
RG 	Char10 	X 
CPF 	Char10 	X 
Data da venda 	dats 	 
Produto 	Char30 	 
Valor de venda 	Curr10 com 2 decimais 	 
 
PROGRAMA – SE38 
Criar novo programa para cadastro de cliente e cadastro de vendas. 
 
A tela de seleção deverá conter 3 opções: 
  
Se a opção “Cadastrar cliente” estiver marcada, deverá aparecer os campos conforme abaixo, todos do tipo parameter : OK 
Campos para cadastrar cliente 
Campo Parameter 	type 	obrigatório 
Nome do Cliente 	Tabela nova 	X 
RG 	Tabela nova 	X 
CPF 	Tabela nova 	X 
Endereço 	Tabela nova 	 
email 	Tabela nova 	 
telefone 	Tabela nova 	 
 
Se a opção “Cadastrar venda” estiver marcada, deverá aparecer os campos conforme abaixo, todos do tipo parameter : ok 
Campos para cadastrar venda 
Campo Parameter 	type 	obrigatório 
RG 	Tabela nova 	X 
CPF 	Tabela nova 	X 
Data da venda 	Tabela nova 	x 
Produto 	Tabela nova 	x 
Valor de venda 	Tabela nova 	x 
 
Se a opção “Relatório de vendas” estiver marcada, deverá aparecer os campos conforme abaixo: 
Campos para relatório 
Campo Parameter 	type 	tipo 
cód da venda 	Tabela nova 	Select-options 
RG 	Tabela nova 	Select-options 
CPF 	Tabela nova 	Select-options 
Data da venda 	Tabela nova 	Select-options 
Produto 	Tabela nova 	Select-options 
  
REGRAS DE TELA: 
Se a opção “Cadastrar cliente” estiver marcada, os parâmetros a serem exibidos deverão ser apenas os referentes a “Campos para cadastrar cliente” os demais campos deverão ficar invisíveis. 
Senão, se a opção “Cadastrar venda” estiver marcada, os parâmetros a serem exibidos deverão ser apenas os referentes a “Campos para cadastrar venda” os demais campos deverão ficar invisíveis. 
Senão, se a opção “Relatório de vendas” estiver marcada, os parâmetros a serem exibidos deverão ser apenas os referentes a “Campos para relatório” os demais campos deverão ficar invisíveis. OK 
 
 
 
REGRAS DO PROGRAMA: 
 Se a opção “Cadastrar cliente” estiver marcada, deverá ser verificado se o registro informado na tela, existe na tabela nova de cadastro de cliente. 
se existir, deverá exibir mensagem ‘Cliente já cadastrado’. 
Se não existir, deverá ser inserido o novo registro, na tabela nova. 
 
CADASTRAR VENDA 
Se a opção “Cadastrar venda” estiver marcada, deverá ser verificado se o registro informado na tela, existe na tabela nova de cadastro de venda. 
Se existir, deverá exibir mensagem do tipo POP-UP ‘Venda já cadastrada, deseja modificar?’. POP-UP terá a opção “sim ou não”. Se o usuário responder “sim”, deverá modificar o registro na tabela. 
Se não existir, deverá ser inserido o novo registro, na tabela nova. 
 
RELATÓRIO DE VENDAS 
Se a opção “Relatório de vendas” estiver marcada, o sistema deverá  buscar na tabela de cadastro de vendas, os registros de acordo com os dados informados na tela de seleção. Com os registros de vendas encontrados, o sistema deverá buscar os dados dos clientes, na tabela nova de cadastro de clientes. 
Com os dados encontrados, exibir um relatório 	com os campos: 
Campo 	Tabela 
cód da venda 	VENDA 
Produto 	VENDA 
Nome do Cliente 	CLIENTE 
RG 	VENDA 
CPF 	VENDA 
Endereço 	CLIENTE 
email 	CLIENTE 
telefone 	CLIENTE 
Valor da venda 	VENDA 
 
SE NÃO ENCONTRAR REGISTROS, DAR MENSAGEM DE ERRO, ‘NENHUM REGISTRO ENCONTRADO’ 
  
