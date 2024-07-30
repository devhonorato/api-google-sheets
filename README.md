# Sheets
 
### API Google Sheets

 
Este código é um aplicativo `Node.js` utilizando o framework `Express`. 

Ele se conecta a uma planilha do `Google Sheets` através da biblioteca de `APIs do Google` e expõe algumas rotas HTTP para recuperar e alterar dados da planilha.

- Rota `/metadata` recupera os metadados da planilha. 

- Rota `/getRows` recupera os dados da primeira página da planilha. 

- Rota `/addRow` adiciona uma nova linha ao final da primeira página da planilha, com os valores enviados no corpo da requisição. 

- Rota `/updateValue` atualiza os valores de uma célula específica da primeira página da planilha, também com os valores enviados no corpo da requisição.

Para autenticar as chamadas à `API do Google Sheets`, o código carrega as credenciais a partir do arquivo [credentials.json](https://developers.google.com/sheets/api/quickstart/go?hl=pt-br#enable_the_api) e cria um objeto de autenticação usando a classe `GoogleAuth`. 

Em seguida, ele cria um cliente de API e um objeto de `API do Google Sheets`, que são utilizados nas rotas para fazer as chamadas à API. 

O `ID` da planilha é armazenado na variável `spreadsheetId`, que deve ser preenchida com o `ID` da planilha desejada antes de usar o aplicativo.

