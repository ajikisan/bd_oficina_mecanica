### Desafio Construindo um Esquema Conceitual para Banco De dados - Oficina Mecânica
<p>Aluna: Mirian Ajiki Molicawa </p>
<p>Digital Innovation One </p>

<h2> Tecnologias </h2>
<br> - Navegador Microsoft Edge
<br> - [BD_Designer](https://app.dbdesigner.net/) 


<h2> Objetivo </h2>
Criar o esquema conceitual para o contexto de oficina com base na narrativa fornecida.

<h2>Narrativa: </h2>
Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas
Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços
A mesma equipe avalia e executa os serviços
Os mecânicos possuem código, nome, endereço e especialidade
Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

<h2>DBDesigner </h2>
DBDesigner é uma ferramenta para projeto de banco de dados que integra a
modelagem, projeto, implementação e manutenção em um mesmo ambiente.
O DBDesigner é OpenSource distribuído sobre a licença GPL General Public Lincense. Permite engenharia reversa, gerando o modelo a partir das tabelas do Banco de Dados e faz a sincronia no BD das alterações realizadas no DER - Diagrama de Entidade e Relacionamento.

<h2>Tabelas e Atributos</h2>

[BD_Oficina_Mecanica](https://app.dbdesigner.net/designer/schema/0-untitled-56ca0624-ec99-463c-81ee-7ffb314c56d3)


![BD_Oficina_Mecanica](https://user-images.githubusercontent.com/91148791/190939578-228afdeb-5541-49f1-b66b-538b0cadc215.png)

<b>Cliente</b>
Nome_Cliente
CPF
Endereco
Telefone
Email
ID_Cliente
RG
Data_Cadastro
<p>
<b>Mecanico</b>
ID_Mecanico
Codigo_Mecanico
Nome_Mecanico
Endereco
Telefone
Especialidade
Endereco
ID_Endereco

<b>Endereco</b>
Bairro
Cidade
Estado
CEP
Complemento

<b>Veiculo_Moto</b>
Marca
Modelo
Ano_Fabricacao
Nome_Cliente
ID_Veiculo_Moto
ID_Cliente

<b>Ordem_Servico</b>
ID_Ordem_Servico
Descricao
Valor_Ordem_Servico
ID_Cliente
ID_Mecanico
Data_Emissao_OS
Forma_Pagamento
Status_Ordem_Servico
Numero_Ordem_Servico
Data_Conclusao_OS
Tipo_Ordem_Servico
Autorizacao_OS
Valor_Pagamento_OS

<b>Produtos_Automotivos</b>
ID_Produto_Automotivo
Descricao_Produto
Categoria_Produto
Valor_Produto
Quantidade
ID_Cliente

<b>Servicos_Automotivos</b>
ID_Servico_Automotivo
Descricao_Servico_Automotivo
Valor_Servico_Automotivo
Data_Servico_Automotivo
ID_Cliente

<b>Mao_Obra</b>
Valor_Total
Data_Mao_Obra
ID_Ordem_Servico
ID_Mao_Obra
ID_Produto_Automotivo
ID_Servico_Automotivo
ID_Cliente
Descricao_Mao_Obra
 
