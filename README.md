# Instagram - DigitalInnovationOne - Augusto Becker #
Projeto prático do bootcamp HTML developer com o objetivo de recriar a página inicial do Instagram. 

## Página Inicial do Instagram ##


   Com base no projeto da dev Gabriela Pinheiro que deu as instruções para o projeto e na própria página original do Instagram criei essa releitura.
Um dos meus maiores desafios foi aprender a lidar com o Flexbox de modo que deixasse a página responsiva.  Após uma série de consultas online à w3schools, mozilla developer network, Khan Academy, alguns canais do Youtube (Rocketseat e Alura) e minhas próprias anotações.
Queria fazer com que o tamanho do container que abrigava toda a div de login, logout, recuperação de conta e download não se alterasse independente do tamanho da tela. Meu erro era ou tirar tudo da porcentagem (o que acabava com a responsividade e mesmo quando funcionava me parecia uma prática ruim) ou colocar tudo em porcentagem (o que não mantinha a div com tamanho fixo).
A solução foi manter a altura em porcentagem e alterar para um valor fixo em px apenas a largura dos container com a div que eu queria manter fixo(.instagram-continue). Já a largura do container maior(.instagram-wrapper) eu coloquei um valor fixo pra manter o espaçamento entre a a div com imagem de celular e a div instagram-continue constante. O mesmo conceito foi utilizado para manter os botões de download igualmente distantes.


.instagram-wrapper { 
    height: 100%;
    width: 900px;
}

.instagram-continue {
    min-height: 35rem;
	width: 350px;
}

Acabou resolvendo a questão e facilitado ainda mais o projeto - que agora precisa apenas de uma media query para max-width: 800 (No começo do projeto eram duas).
Um outro obstáculo era criar um footer e mantê-lo responsivo. Ele não estava no projeto inicial mas quis incorporá-lo para ser mais fiel à página do Instagram.
Criar uma outra div e deixar que o conteúdo ficasse disperso em duas grandes divs me causou problemas com a responsividade das duas. Resolvi o problema colocando todos os componentes dentro da mesma div e quebrando uma linha para fazer o Footer.

flex-wrap: wrap;

Para fazer com que alguns links ficassem com uma cor de fonte mais clara (e fundo também, em uma ocasião) enquanto fossem clicados usei uma pseudo-classe.

a:active{  ...  }
