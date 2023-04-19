# Netlfix-Challenge - APS5_ALGLIN

Esse é um projeto da matéria de Algebra Linear e Teoria da Informação do Insper para o curso de Ciência da Computação.

# Projeto: Desafio Netflix

Neste projeto, trabalharemos com o [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset), que possui a avaliação de usuários em relação a filmes. Utilizando o csv `ratings_small.csv`, presente neste dataset.

## Descrição do Projeto

Enunciado: Um problema que existe hoje em dia com as grandes empresas de streaming (Netflix, Spotify, etc.) é que elas têm um acervo de conteúdo muito grande, e os usuários tendem a gostar, cada um, de uma pequena parte desse acervo. Então, como poderíamos escolher quais filmes vão aparecer tela inicial do seu streaming?

O projeto consiste em fazer a implementação de um sistema preditor de nota de filmes por usuário, o sistema projetado deve ser avaliado usando um histograma dos erros ao longo de várias estimativas. O número de estimações deve ser, no mínimo, mil.

## Descrição Matemática 

O modelo matemático utilizado para o desenvolvimento do projeto foi baseado na ideia de que o sistema de recomendação utiliza "perfis" típicos de usuários. Os perfis, são vetores que mostram que notas são tipicamente atribuídas para cada filme por usuários daquele perfil. Por exemplo, talvez tenhamos dois perfis e três filmes, e nesse caso poderíamos ter os perfis:

* $p_0 = [2, 5, 2]$, isto é, o perfil $0$ é de uma pessoa que gosta muito do filme $f_1$, e
* $p_1 = [5, 0, 4]$, isto é, o perfil $1$ é de uma pessoa que gosta dos filmes $f_0$ e $f_2$. 

Porém, sabemos que usuários reais raramente se comportam estritamente como um perfil. As notas realmente atribuídas por um usuário aos filmes, então, são modeladas como combinações lineares dos perfis. Por exemplo, podemos ter usuários:

* $u_0 = 0.1 p_0 + 0.9 p_1$, para um usuário muito próximo de $p_1$ mas distante de $p_0$,
* $u_1 = 0.1 p_0 + 0.1 p_1$, para um usuário distante tanto de $p_0$ quanto de $p_1$,

Então, o que precisamos é de uma maneira de mapear usuários para perfis, e então perfis para filmes. Precisamos então *decompor* nossa matriz $A$ de usuários $\times$ filmes em componentes:

$A = X Y Z$,

onde:
* $A$ tem uma linha por usuário e uma coluna por filme,
* $X$ tem uma linha por usuário e uma coluna por perfil,
* $Y$ é quadrada e mapeia perfis para perfis,
* $Z$ tem uma linha por perfil e uma coluna por filme.

## Como rodar o projeto e Funcionalidades

### Clone o repositório do nosso projeto:

```py
https://github.com/WeeeverAlex/Netlfix-Challenge
```

### Depois instale os requirements:

```py
pip install -r requirements.txt
```

## Por fim, basta executar o arquivo demo.py: 

```py
python demo.py
```
O projeto possui as seguintes funcionalidades:

## Resultado final

## Autores

- [@st4pzz](https://github.com/st4pzz)
- [@WeeeverAlex](https://github.com/WeeeverAlex)

