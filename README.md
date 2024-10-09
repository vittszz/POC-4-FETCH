# POC-4-FETCH

Funcionamento:

1 - Estrutura HTML (CABEÇALHO)
Cabeçalho (head): Aqui, definimos o charset, a viewport (para garantir que a página funcione bem em dispositivos móveis) e o título da página. Adicionamos também algumas regras de estilo para a formatação.
![image](https://github.com/user-attachments/assets/fbf83519-3e06-491b-b466-e16537c7588e)

Corpo (body):

Temos um título (<h1>) e um parágrafo (<p>) para descrever o objetivo da página.

O botão Get Random User dispara a ação de buscar os dados.

A div com o ID userInfo é onde os dados serão exibidos.


O que é FETCH?
O método fetch é uma função nativa do JavaScript que permite fazer requisições HTTP assíncronas a servidores. Ele retorna uma Promise, que representa uma operação que será resolvida (com sucesso) ou rejeitada (com erro) no futuro. A Promise permite que lidemos com respostas assíncronas usando .then() ou await.

2 - Estrutura HTML:

Criamos um layout simples com um botão (Get Random User) e uma div vazia onde as informações do usuário aleatório serão exibidas após a requisição.

O estilo foi adicionado diretamente no arquivo para garantir uma boa apresentação (ex: imagem do usuário redonda, borda na div).

![image](https://github.com/user-attachments/assets/1d36a7b8-801c-4366-84f5-bf1708a620a6)


3 - Função fetchRandomUser:

Passo 1:
Quando o botão é clicado, a função fetchRandomUser é chamada.

Adicionamos uma mensagem de "Loading..." no contêiner para informar o usuário que os dados estão sendo buscados.

Passo 2:
A função faz uma requisição HTTP GET usando fetch('https://randomuser.me/api/'). Esse método retorna uma Promise.

Usamos await para esperar a resolução da Promise. Com isso, o código aguarda até que a resposta seja recebida da API antes de prosseguir.

Passo 3:
Verificamos se a resposta foi bem-sucedida usando response.ok. Caso contrário, um erro é gerado.

A função response.json() também é chamada com await, para extrair o conteúdo JSON da resposta.

Passo 4:
Após receber os dados JSON, extraímos o primeiro usuário (data.results[0]) e pegamos informações como nome, email, país e foto.

Passo 5:
Usamos a manipulação do DOM para preencher a div com essas informações. Inserimos um <img> para a foto do usuário e vários <p> para o nome, email e país.

Passo 6:
Caso ocorra algum erro durante a requisição ou a extração dos dados, ele é capturado pelo catch, e uma mensagem de erro é exibida ao usuário.

4 - Execução da POC:

Quando o usuário clica no botão "Get Random User", a função faz a requisição e, enquanto aguarda a resposta, exibe "Loading...".

Assim que a resposta chega, o usuário aleatório é exibido, com nome, email, país e uma foto.

Se houver falhas (como problemas de rede), uma mensagem de erro é exibida na tela.

![image](https://github.com/user-attachments/assets/c90b9936-ac7a-4c1d-b18b-140d7eb7f6ce)


5 - Fluxo Assíncrono com fetch e async/await:

![image](https://github.com/user-attachments/assets/02ab4f0a-c30e-4d9a-be8a-c9c41fc8fb1d)

Seleção de Elementos: Usamos getElementById para selecionar o botão (fetchButton) e o contêiner onde as informações serão exibidas (userInfoDiv).

Adicionando o Evento: O método addEventListener escuta o clique no botão e chama a função fetchRandomUser.

Função fetchRandomUser:

Mostrando "Loading...": Assim que a função é chamada, alteramos o conteúdo da div para "Loading..." enquanto os dados da API estão sendo buscados.

Usando fetch: O método fetch faz a requisição HTTP para a API. O await garante que o código espere a resposta antes de continuar.

Erro HTTP: Se a resposta não for bem-sucedida (status diferente de 200), lançamos um erro.

Conversão para JSON: Após receber a resposta, convertemos para JSON com await response.json().

Manipulação do DOM: Pegamos os dados do usuário e os exibimos no contêiner userInfoDiv usando innerHTML.

Tratamento de Erros: Se ocorrer qualquer erro durante o processo, mostramos uma mensagem de erro amigável.
