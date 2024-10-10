#POC 4 - FETCH

Estrutura HTML: 

![image](https://github.com/user-attachments/assets/0a5adabe-be30-4aec-bf16-90fac3f5b261)

O que faz essa parte?

Cabeçalho HTML: Define o charset (UTF-8) e configurações de viewport para uma melhor responsividade.
CSS embutido: Define o estilo básico da página, como o estilo do corpo, imagem do usuário (arredondada), e o layout do contêiner onde os dados do usuário serão exibidos.

JavaScript - Função 

![image](https://github.com/user-attachments/assets/11018793-e34c-410f-b15f-7722d9a0060b)

Seleção de Elementos: document.getElementById() para pegar o botão que será clicado (fetchButton) e o contêiner que exibirá os dados do usuário (userInfoDiv).
Evento de Clique: Quando o botão é clicado, ele aciona a função fetchRandomUser().



Função do Fetch Assincrona:
![image](https://github.com/user-attachments/assets/1d803b24-8f6b-4eaa-a28c-e16235bc0d7f)

A função principal que faz o fetch dos dados é escrita usando async/await, o que simplifica o tratamento de promessas.

Mensagem de Carregamento: Quando o botão é clicado, o texto "Loading..." é exibido no contêiner enquanto a API está sendo chamada.

Requisição à API: O fetch realiza uma requisição GET para a API randomuser.me. A função aguarda a resposta com await.

Tratamento de Erros: Se a resposta da API falhar (status diferente de 200-299), um erro é gerado e tratado no bloco catch.

Exibição dos Dados: Quando a resposta é convertida para JSON, os dados do primeiro usuário são extraídos e exibidos dinamicamente no DOM (nome, e-mail, país, e imagem).

Exibição do DOM:
![image](https://github.com/user-attachments/assets/2233eacc-9cae-4a82-a72b-ee33f5be3cb7)

Imagem do Usuário: Exibe a foto de perfil retornada pela API.
![image](https://github.com/user-attachments/assets/d5c45b7e-f595-4abb-b708-38efd4537ed2)

Nome, E-mail e País: Mostra as informações de nome completo, e-mail e país de origem.

Conclusão da POCç
Este projeto simples de POC usa o Fetch API para obter dados de forma assíncrona de uma API externa. A função fetchRandomUser trata de fazer a requisição, processar os dados e atualizar a interface do usuário com as informações recebidas.

#PRINT DA EXECUÇÃO DO CODIGO: 

![image](https://github.com/user-attachments/assets/849e982f-d25d-4c5a-8372-73bc774d8b5c)




