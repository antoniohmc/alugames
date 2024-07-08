Projeto de Aluguel de Jogos
Bem-vindo ao projeto de aluguel de jogos! Este projeto tem como objetivo criar uma plataforma para alugar e devolver jogos de forma simples e intuitiva.

Funcionalidades
Listar Jogos: Exibe uma lista de jogos disponíveis para aluguel.
Alugar Jogo: Permite que o usuário alugue um jogo.
Devolver Jogo: Permite que o usuário devolva um jogo alugado.
Tecnologias Utilizadas
HTML: Para a estrutura da página.
CSS: Para o estilo da página.
JavaScript: Para a interatividade da página.

Como Utilizar
1. **Clone o repositório:**
git clone https://github.com/antoniohmc/projeto-aluguel-jogos.git

2.**Abra o arquivo index.html no seu navegador:**
open index.html

3.**Interaja com a plataforma:**

* Clique no botão "Alugar" para alugar um jogo.
* Clique no botão "Devolver" para devolver um jogo alugado.
** Função alterarStatus **
Esta função é responsável por alterar o status de aluguel dos jogos.

function alterarStatus(id) {
    let gameClicado = document.getElementById(`game-${id}`);
    let imagem = gameClicado.querySelector('.dashboard__item__img');
    let botao = gameClicado.querySelector('.dashboard__item__button');
    let nomeJogo = gameClicado.querySelector('.dashboard__item__name');

    if (imagem.classList.contains('dashboard__item__img--rented')) {
        imagem.classList.remove('dashboard__item__img--rented');
        botao.classList.remove('dashboard__item__button--return');
        botao.textContent = 'Alugar';
    } else {
        imagem.classList.add('dashboard__item__img--rented');
        botao.classList.add('dashboard__item__button--return');
        botao.textContent = 'Devolver';
    }
}

* Parâmetro id: O ID do jogo que está sendo alterado.
* Lógica: A função verifica se o jogo está alugado ou não e altera a classe e o texto do botão de acordo com o status atual.
