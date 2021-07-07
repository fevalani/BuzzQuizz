<h1 align="center">
    Projeto-BuzzQuizz
</h1>

<p align="center"> <a href="https://github.com/">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/fevalani/Projeto-BuzzQuizz?style=for-the-badge">
  </a>
</p>

<h4 align="center"> 
	 Status: Entregue.
</h4>

## Sobre

Quinto projeto realizado durante o **Bootcamp Responde Aí** do [Responde Aí](https://page.respondeai.com.br/bootcamp). <br>

Primeiro projetão, realizado em dupla, foi a implementação de um sistema de Quizzes em HTML, CSS e JavaScript! Nesse sistema, fomos responsáveis por desenvolver tanto a experiência do Quiz em si, quanto as telas que permitem criar quizzes!
---

## Requisitos

- Tela 1: Lista de Quizzes
    - [x]  Nesta tela, devem ser listados os quizzes fornecidos pelo servidor, seguindo o layout dado
    
    - [x]  A lista de quizzes do usuário deve mostrar somente seus quizzes, enquanto a lista de baixo deve mostrar todos os quizzes recebidos, sem os do usuário. Para diferenciar os quizzes do usuário dos demais, veja o requisito **Quizzes do Usuário**
    
    - [x]  Os quizzes devem ser exibidos num formato retangular (conforme layout), com a imagem e título do quizz. A imagem deve estar sobreposta com um degradê de preto para transparente conforme layout. Ao clicar sobre o quizz, esta tela deve sumir e dar lugar à **Tela 2: Página de um quizz** do quizz em questão

    - [x]  Ao clicar em "Criar Quizz" ou no "+" essa tela deve sumir, dando lugar à tela de **Tela 3: Criação de Quiz**


- Tela 2: Página de um quizz (perguntas)
    - [x]  No topo do quizz, deve ser exibido um banner com a imagem e o título do quizz. A imagem deve estar escurecida com uma camada preta de 60% de opacidade.
    
    - [x]  As respostas de cada pergunta devem ser exibidas organizadas aleatoriamente
    
    - [x]  Ao clicar em uma resposta, as demais devem ganhar o efeito "esbranquiçado" do layout
    
    - [x]  Não deve ser possível alterar a resposta após a escolha
    
    - [x]  Após escolher uma resposta, o texto das opções deve ganhar a cor vermelha ou verde, conforme layout, indicando quais eram as respostas erradas e a certa
    
    - [x]  Após 2 segundos de respondida, deve-se scrollar a página para a próxima pergunta


- Tela 2: Página de um quizz (fim do quizz)
    - [x]  Após responder todas as perguntas, deve aparecer ao final da tela a caixa de resultado do quizz. Assim como na passagem das perguntas, deve-se aguardar 2 segundos após a última resposta e então scrollar a tela para exibir essa caixa de resultado
    
    - [x]  A pontuação do quiz (porcentagem de acertos sobre total de perguntas) deve ser calculada no front, sem nenhuma comunicação com o servidor, bem como a classificação de em qual nível o usuário ficou baseado nessa pontuação
    
    - [x]  Deverão ser exibidos o título, a imagem e a descrição do nível que o usuário ficou
    
    - [x]  O score deve ser arredondado de forma a não ter casas decimais
    
    - [x]  Ao clicar no botão "Reiniciar Quizz", a tela deverá ser scrollada novamente para o topo, as respostas zeradas pro estado inicial e a caixa de resultado escondida novamente
    
    - [x]  Ao clicar no botão "Voltar pra home", essa tela deve sumir e dar lugar à **Tela 1: Lista de Quizzes**


- Tela 3: Criação de Quiz
    - [x]  O processo de criar um quizz passará por 4 telas, seguindo o layout:
        - Tela 3.1: Informações básicas do quizz
        - Tela 3.2: Perguntas do quizz
        - Tela 3.3: Níveis do quizz
        - Tela 3.4: Sucesso do quizz
    
    - [x]  A cada etapa, antes de avançar para a próxima tela, devem ser feitas validações nas informações inseridas, seguindo as regras abaixo:
        - Informações básicas do quizz
            - [x]  Título do quizz: deve ter no mínimo 20 e no máximo 65 caracteres
            - [x]  URL da Imagem: deve ter formato de URL
            - [x]  Quantidade de perguntas: no mínimo 3 perguntas
            - [x]  Quantidade de níveis: no mínimo 2 níveis
        
        - Perguntas do quizz
            - [x]  Texto da pergunta: no mínimo 20 caracteres
            - [x]  Cor de fundo: deve ser uma cor em hexadecimal (começar em "#", seguida de 6 caracteres hexadecimais, ou seja, números ou letras de A a F)
            - [x]  Textos das respostas: não pode estar vazio
            - [x]  URL das imagens de resposta: deve ter formato de URL
            - [x]  É obrigatória a inserção da resposta correta e de pelo menos 1 resposta errada. Portanto, é permitido existirem perguntas com só 2 ou 3 respostas em vez de 4.
        
        - Níveis do quizz
            - [x]  Título do nível: mínimo de 10 caracteres
            - [x]  % de acerto mínima: um número entre 0 e 100
            - [x]  URL da imagem do nível: deve ter formato de URL
            - [x]  Descrição do nível: mínimo de 30 caracteres
            - [x]  É obrigatório existir pelo menos 1 nível cuja % de acerto mínima seja 0%
    
    - [x]  Caso alguma validação falhe, deve ser exibida um alerta pedindo para o usuário preencher os dados corretamente. Para simplificar, não é obrigatório informar qual foi a validação que falhou.
    
    - [x]  Ao finalizar a criação do quizz e salvá-lo no servidor, o usuário deverá visualizar a **Tela 3.4: Sucesso do quizz**. Nesta tela ele pode clicar no quizz (ou no botão de "Acessar Quizz") para visualizar o quizz criado (Tela 2) ou voltar pra home (Tela 1)
    
    - [x]  Quando o usuário retornar pra home (seja imediatamente ou mais tarde), esta deve atualizar os quizzes listados para incluir o quizz recém-criado


- Quizzes do Usuário
    - [x]  Ao criar um quizz no servidor, este devolverá como resposta o objeto completo do quizz criado, incluindo o id (identificador único) que o servidor gerou pra este quizz
    
    - [x]  Para futuramente você conseguir diferenciar um quizz criado pelo usuário de outros quizzes, você pode armazenar esses ids no momento da criação do quizz

    - [x]  Na Tela 1: Lista de Quizzes, você pode comparar o id dos quizzes vindo do servidor com esses ids armazenados na criação dos quizzes para verificar se um determinado quizz foi criado pelo usuário em questão
---

## Layout

O layout da aplicação se encontra no Figma:

<a href="https://www.figma.com/file/nCuPD1re0r4EAwNl7OCNvz/BuzzQuizz---Turma-02?node-id=0%3A1">
  <img alt="Project Figma" src="https://img.shields.io/badge/%20Layout%20-Figma-%2304D361?style=for-the-badge&logo=appveyor">
</a>


### Desktop

<p align="center">
  <img alt="Desktop Homepage" title="#Homepage" src="imagens/readme.png" width="400px" height="355px">
  <img alt="Desktop Homepage" title="#Homepage" src="imagens/readme2.png" width="400px" height="355px">
</p>


### Mobile

<p align="center">
  <img alt="Mobile Homepage" title="#Homepage" src="imagens/readme3.png" width="200px" height="355px">
  <img alt="Mobile Homepage" title="#Homepage" src="imagens/readme4.png" width="200px" height="355px">
</p>

## Tech Used

Foram usadas as seguintes ferramentas para o desenvolvimento do projeto:

- **[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://html5.org/)**
- **[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/Overview.en.html)**
- **[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://www.javascript.com/)**

#### **Utilities**

- Prototype: **[Figma](https://www.figma.com/)** → **[Protótipo (BuzzQuizz)](https://www.figma.com/file/nCuPD1re0r4EAwNl7OCNvz/BuzzQuizz---Turma-02?node-id=0%3A1)**
- Editor: **[Visual Studio Code](https://code.visualstudio.com/)**
- Fonts: **[Roboto](https://fonts.google.com/specimen/Roboto)**

---

## Authors

<p style="display: flex; flex-direction: row;">
<a style="border-radius: 50px;" width="100px;" href="https://github.com/fevalani">
 <img style="border-radius: 50px;" src="https://avatars.githubusercontent.com/u/81244714?v=4" width="100px;" alt="Fernando Valani"/>
 <br />
 <sub><b>Fernando Valani</b></sub></a>
 <br />
 
<a style="border-radius: 50px;" width="100px;" href="https://github.com/yungtay">
 <img style="border-radius: 50px;" src="https://avatars.githubusercontent.com/u/81389071?v=4" width="100px;" alt="Fernando Valani"/>
 <br />
 <sub><b>Christian Yungtay</b></sub></a>
 <br />

## </p>

## License

👋🏽 Get in Touch!

---
