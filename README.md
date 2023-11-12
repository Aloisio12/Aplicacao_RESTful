TÍTULO DO PROJETO:
Aplicação RESTful utilizando Node.js, Express e Prisma
<br><br>
EXPLICAÇÃO:
Uma aplicação RESTful API é um serviço web que segue os princípios da arquitetura REST (Representational State Transfer). Essa abordagem utiliza URLs únicas para identificar recursos, opera através de métodos HTTP padrão (como GET, POST, PUT e DELETE) para realizar operações CRUD, utiliza representações de recursos em formatos como JSON ou XML, é stateless (sem manter estado entre solicitações), e promove a consistência nas respostas HTTP. É uma forma eficiente e escalável de criar serviços web, frequentemente usada para integração entre sistemas e desenvolvimento de aplicações web modernas.
<br><br>
Usaremos dois sites importantes para a contrução da aplicação, são eles:
<br><br>
Prisma Studio:
É uma interface visual para explorar e manipular dados em seus projetos Prisma. É uma ferramenta ORM (Object-Relational Mapping) de próxima geração para JavaScript e TypeScript. Com uma interface tabular simples, você pode rapidamente dar uma olhada nos dados do seu banco de dados local e verificar se seu aplicativo está funcionando corretamente. Ele permite a visualização de dados de qualquer maneira que você desejar, filtrando, classificando e paginando. Além disso, o Prisma Studio facilita o acesso e a navegação de dados relacionados de ambos os lados da relação. Você pode editar com segurança no local, como em planilhas, clicando duas vezes em uma célula e editando seu valor no local. Ele também suporta o tema escuro.
<br><br>
Neon.tech:
É um serviço de banco de dados Postgres sem servidor, tolerante a falhas e com capacidade de ramificação. Ele separa armazenamento e computação para oferecer escalabilidade sob demanda, ramificação e armazenamento sem limites. O Neon é compatível com o cliente Postgres porque um cálculo Neon é Postgres. O Neon ajusta dinamicamente a alocação de recursos de computação com base na carga de trabalho. Ele foi projetado desde o início como um sistema tolerante a falhas e escalável para a nuvem. Ele integra-se com lojas de objetos em nuvem, como o S3, para descarregar dados frios para otimização de custos. O Neon permite que você ramifique instantaneamente seu banco de dados Postgres para suportar fluxos de trabalho de desenvolvimento modernos.
<br><br>
PRÉ-REQUISITOS:
<br><br>
- Visual Studio e sua extensão "restClient":
Ferramenta de desenvolvimento integrado (IDE) da Microsoft com uma extensão que permite testar APIs REST diretamente do ambiente de desenvolvimento.
<br><br>
- Node: 
Ambiente de execução JavaScript do lado do servidor, permitindo o desenvolvimento de aplicativos web escaláveis.
<br><br>
- Express:
Framework web para Node.js que simplifica a criação de aplicativos web e APIs, proporcionando uma estrutura robusta e flexível.
<br><br>
INSTALAÇÃO:
<br><br>
Visual Studio:
Baixe e instale através do link:
https://visualstudio.microsoft.com/pt-br/
<br><br>
Node:
<br><br>
Baixe o gerenciador de versões do Node através do terminal:
Comando para Windows:
iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.ps1'))
<br><br>
Comando para Linux e Mac OS:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
<br><br>
No terminal, instale a versão mais recente do Node:
nvm install node
<br><br>
Express:
No terminal do Visual Studio, insira o seguinte comando:
npm install express
<br><br>
restClient:
Acesse a aba de extensões do Visual Studio na lateral esquerda e insira o nome "restClient", instale a extensão
<br><br>
TypeScript:
no terminal do Visual Studio, digite:
npm install tyscript ts-node @types/node --save-dev
<br><br>
COMEÇANDO:
<br><br>
Inice o Node no projeto no terminal do Visual Studio:
npm init -y
<br><br>
Inicie o TypeScript no terminal do Visual Studio:
npx tsc --init
<br><br>
Iniciando Prisma no terminal do Visual Studio:
npx prisma init
<br><br>
Iniciando no site Neon.tech:
Criar uma Conta:
<br><br>
Vá para https://console.neon.tech/ em seu navegador.
Encontre a Opção de Registro:
Geralmente, há um botão ou link para "Registro" ou "Criar Conta". Clique nesse botão.
Preencha o Formulário de Registro
<br><br>
Você será solicitado a fornecer informações como nome, endereço de e-mail e criar uma senha. Preencha o formulário com informações precisas.
Verifique Seu E-mail (Se Necessário):
<br><br>
Algumas plataformas exigem que você verifique seu endereço de e-mail. Se for o caso, vá até sua caixa de entrada de e-mail e siga as instruções fornecidas.
Faça Login na Sua Nova Conta:
<br><br>
Após a verificação, retorne ao site e faça login usando as credenciais que você acabou de criar.
<br><br>
Criar um Novo Projeto:
Faça Login na Sua Conta
<br><br>
Se ainda não estiver logado, entre na sua conta usando suas credenciais.
Navegue até a Página de Projetos:
<br><br>
Procure por uma seção chamada "Projetos" ou algo similar. Pode estar no painel de controle principal.
Encontre a Opção para Criar um Novo Projeto:
<br><br>
Dentro da seção de projetos, geralmente há um botão ou link para "Criar Novo Projeto" ou algo semelhante. Clique nesse botão.
Preencha as Informações do Projeto:
<br><br>
Você será solicitado a fornecer informações sobre o novo projeto, como nome, descrição, e talvez outras configurações específicas do projeto. Preencha essas informações conforme necessário.
Confirme e Crie o Projeto:
<br><br>
Revise as informações do projeto para garantir que estejam corretas. Em seguida, clique em um botão ou link para confirmar e criar o projeto.
<br><br>
Inicialize o Prisma Studio no terminal do Visual Studio:
npx prisma studio
<br><br>
Ele irá abrir uma página na web igual ou parecida com esta:
http://localhost:5555/
<br><br>
TESTE DO PROJETO:
No arquivo routes.http, faça o seguinte:
<br><br>
Certifique-se de que sua aplicação Node.js esteja em execução em http://localhost:3333. Se não estiver, ajuste o endereço da URL nas chamadas conforme necessário.
Postagem dos Dados:
<br><br>
Abra o arquivo routes.http onde você está mantendo suas solicitações no Visual Studio Code.
<br><br>
Coloque o código de postagem dos dados:
<br><br>
POST http://localhost:3333/client<br>
Content-Type: application/json<br>
{
  "name": "Wendell Silva Sales",
  "email": "wendellsilva@gmail.com"
}
<br>Execute a solicitação clicando em Send Request.
<br><br>
***Recebimento dos Dados:
<br><br>
Coloque o código para obter todos os clientes:
<br><br>
###<br>
GET http://localhost:3333/client
Execute a solicitação clicando em Send Request.
<br><br>
***Recebimento dos Dados por ID:
<br><br>
Coloque o código para obter um cliente por ID (substitua 2 pelo ID desejado):
<br><br>
###<br>
GET http://localhost:3333/client/2
<br><br>
Execute a solicitação clicando em Send Request.
<br><br>
***Atualização de Dados:
<br><br>
Coloque o código para atualizar dados (substitua 2 pelo ID desejado):
<br><br>
###<br>
PUT http://localhost:3333/client/2<br>
Content-Type: application/json<br>
{
  "name": "Jennifer Silva Sales",
  "email": "jennifersilva@gmail.com"
} 
<br><br>
Execute a solicitação clicando em Send Request.
<br><br>
***Deletar um Dado por ID:
<br><br>
Coloque o código para excluir um cliente por ID (substitua 2 pelo ID desejado):
<br><br>
###<br>
DELETE http://localhost:3333/client/2
<br><br>
Execute a solicitação clicando em Send Request.<br>
Certifique-se de ter "###" antes de cada método de dados(menos antes do primeiro método) para que a aplicação funcione corretamente.
