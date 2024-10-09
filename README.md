POC - Uso da API Fetch com Async/Await

Descrição:
Esta POC demonstra como usar o método assíncrono fetch em JavaScript para fazer requisições HTTP e manipular os dados recebidos. Ela usa a Random User API para obter informações de usuários fictícios, como nome, email, país, e foto. Também exibe essas informações de forma elegante na página.

Estrutura do Código:
HTML: Criação da interface de usuário, incluindo um botão para buscar os dados e uma área onde as informações do usuário serão exibidas.
CSS: Estilos para organizar o layout e garantir que a interface seja visualmente agradável.
JavaScript: Função assíncrona que usa fetch para obter os dados da API e atualiza o conteúdo da página com as informações do usuário.

Explicação do Código:
HTML:
Estrutura: A página contém um título (<h1>), um botão (<button>) e uma div vazia onde as informações do usuário serão exibidas.
Botão: O botão com o ID fetchButton é usado para disparar a requisição à API quando clicado.
Div userInfo: Inicialmente, está oculta com display: none. Quando os dados são carregados, seu conteúdo é atualizado e ela passa a ser visível.

CSS:

Estilos básicos: Definimos estilos para o corpo da página, para o botão, e para a div que exibirá as informações.
Imagem: A imagem do usuário é exibida como um círculo, com largura e altura definidas.
Botão: O botão tem uma cor de fundo azul e fica mais escuro quando o cursor passa por cima (efeito hover).
JavaScript:

Event Listener: O botão dispara a função fetchRandomUser quando clicado.
Função fetchRandomUser:
Carregamento: Exibe "Loading..." enquanto a API está sendo consultada.
Fetch: Faz uma requisição à API https://randomuser.me/api/ usando o método assíncrono fetch.
Verificação de sucesso: Verifica se a resposta foi bem-sucedida usando response.ok. Caso contrário, gera um erro.
Extração de dados: Converte a resposta em JSON e extrai informações como nome, email, país e foto do usuário.
Atualização do DOM: Preenche a div com as informações extraídas.
Tratamento de erros: Caso ocorra um erro, exibe uma mensagem de erro na div.
Como Testar:
Crie um arquivo .html e cole o código acima.
Abra o arquivo no navegador.
Clique no botão "Get Random User" para buscar e exibir as informações de um usuário aleatório.

Conclusão:
Este exemplo simples demonstra como fazer uma requisição assíncrona em JavaScript usando o método fetch e exibir os resultados na página. O uso de async/await torna o código mais limpo e fácil de entender. Além disso, o tratamento de erros garante que a experiência do usuário não seja interrompida de forma abrupta.
