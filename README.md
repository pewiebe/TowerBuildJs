## Desenvolvido por, Leandro, Gabriel, Luiz, Alana e Samuel/Pewiebe

## Tecnologias usadas :computer:
<div style="display: inline_block">
 <img align="center" alt="Lops-HTML" height="30" width="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">-
 <img align="center" alt="Lops-CSS" height="30" width="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">-
 <img align="center" alt="Lops-Js" height="30" width="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
</div> 

# TowerBuild :Torre:

Português

<h1 align="center">Jogo de construção de torres</h1>
<p align="center"><img src="https://o2qq673j2.qnssl.com/tower-loading.gif"/></p>

> um jogo de construção de torres baseado em ES6 e Canvas (Tower Bloxx Deluxe Skyscraper)

## Demo
<p align="center"><img src="https://user-images.githubusercontent.com/17680888/47480922-93a20c00-d864-11e8-8f7c-6d1d60184730.gif"/></p>

<p align="center">

</p>

## Regra do jogo

A seguir estão as regras de jogo padrão:

- Em cada jogo o jogador começa com 3 hp. Toda vez que um bloco de torre é derrubado jogador é deduzido 1 hp; O jogo termina quando o HP está esgotado.

-  O jogador é recompensado com 25 pontos por cada bloco empilhado bem-sucedido (Sucesso). Se um bloco é empilhado pefectly (Perfeito) em cima do anterior, então jogador
recompensado com 50 pontos. Consecutivos Perfects concede 25 pontos adicionais.

**Nota:  Cada Sucesso ou Perfeito constitui um andarr**

  Por exemplo, o primeiro Perfect atribui 50 pontos. A segunda Perfect consecutiva atribui 75 pontos.
 A terceira Perfect consecutiva concede 100 pontos.  etc.

<p align="center">
  <img width="550" src="https://user-images.githubusercontent.com/17680888/47473105-d9021180-d843-11e8-8c19-b6b78d86cbdf.png" />
</p>

## Personalizando a regra do jogo

```
https://github.com/pewiebe/TowerBuildJs.git
cd TowerBuildJs
npm install
npm start
```
Open `http://localhost:8082`  em um navegador da Web.

- Para personalizar arquivos de recursos de imagem e som substitua diretamente o arquivo correspondente em`assets` diretório.
- Para personalizar as regras do jogo, modifique o `option` objeto em `index.html`.

## Opção

Use a tabela a seguir de `option` constantes para completar a personalização das regras do jogo.

**Note: todas as constantes são incluídas opcionalmente**

| Opçãp| Tipo | Descrição |
|---------|--------|-------------|
| width          | number | Width of game interface |
| height         | number | Height of game interface |
| canvasId       | string | DOM ID in Canvas |
| soundOn        | boolean | If sound is on |
| successScore   | number | Points awarded for success |
| perfectScore   | number | Additional points awarded for perfect |
| <a href="#hookspeed">hookSpeed</a> | function | Speed of hook's movement |
| <a href="#hookangle">hookAngle</a> | function | Angle of hook |
| <a href="#landblockspeed">landBlockSpeed</a> | function | Speed of block sway |
| <a href="#setgamescore">setGameScore</a> | function | hook for current score |
| <a href="#setgamesuccess">setGameSuccess</a> | function | hook for number of current succesful game |
| <a href="#setgamefailed">setGameFailed</a> | function | hook for number of current failed game |

#### velocidade do gancho
Velocidade de movimento do gancho
Essa função usa dois parâmetros, currentFloor e currentScore, e retorna um valor de velocidade.
```
function(currentFloor, currentScore) {
  return number
}
```

#### ângulo do gancho
Ângulo do gancho
Essa função usa dois parâmetros, currentFloor e currentScore, e retorna um valor de ângulo.
```
function(currentFloor, currentScore) {
  return number
}
```

#### velocidade do bloco de terra
Velocidade de oscilação do bloco
Essa função usa dois parâmetros, currentFloor e currentScore, e retorna um valor de velocidade.
```
function(currentFloor, currentScore) {
  return number
}
```

#### definir o placar do jogo
gancho para pontuação atual
Essa função recebe um parâmetro, score, e define currentScore como score.
```
function(score) {
  // your logic
}
```

#### definir o sucesso do jogo
gancho para o número de jogos atuais bem-sucedidos
Essa função usa um parâmetro, pontuação, e define GameSuccess como successCount.
```
function(successCount) {
  // your logic
}
```

#### jogo de set falhou
gancho para o número de jogos com falha atual
Essa função recebe um parâmetro, pontuação, e define GameFailed como failedCount.
```
function(failedCount) {
  // your logic
}
```
