# ⚡ Super Desafio Relâmpago — Portfólio Pessoal

## 📌 Introdução

Este repositório contém o desenvolvimento do meu **portfólio pessoal online**, criado como parte de um **desafio relâmpago** com foco em consolidar e praticar fundamentos importantes do desenvolvimento front-end.

Mais do que apenas “entregar um site”, a ideia deste projeto é **demonstrar raciocínio, organização, intenção de design e domínio dos conceitos básicos**, seguindo regras bem definidas e próximas do que é esperado em um cenário real de estudo e apresentação.

Este README foi escrito para cumprir dois papéis ao mesmo tempo:

- 📖 **Documentar o projeto**
- 🧠 **Servir como material de estudo**, explicando decisões, estrutura e conceitos aplicados

A proposta é que qualquer pessoa (inclusive eu mesmo no futuro) consiga ler este arquivo, entender o desafio, o que foi feito e por quê — sem precisar adivinhar nada.

---

## 🧩 Proposta do Desafio

### 1. O que deve ser feito:
Crie seu próprio portfólio online para exibir seus projetos e habilidades.

### 2. Requisitos mínimos:
- Estrutura clara em HTML com uso de tags semânticas.
- CSS bem-organizado, responsivo e animado, a acessibilidade deve ser levada em consideração.
- Deve se utilizar um CSS puro.
- Deve ter um design bem-feito e bem pensado e limpo.
- Deve ser criado um protótipo utilizando Figma.
- O projeto deve ser guardado em um repositório público no GitHub.

---

## 📖 Sobre o projeto

Este projeto foi desenvolvido como parte do **Primeiro Desafio Relâmpago da turma 7** da Alpha Ed/Tech e também será utilizado como **portfólio pessoal online**, onde novos projetos serão adicionados ao longo do período de estudos.

A proposta foi criar um site simples, visualmente marcante e funcional utilizando **HTML semântico e CSS puro**, sem uso de JavaScript, respeitando os critérios técnicos do desafio.

### 🎨 Planejamento visual (Figma)

Antes da implementação, foi criado um **protótipo no Figma**, focado inicialmente apenas na versão desktop.

O layout foi inspirado na *title screen* do jogo **Super Mario World**, um jogo que fez parte da minha infância e serviu como referência estética para o projeto. O background utilizado é uma sprite artística baseada no universo Mario, adaptada para compor o cenário da página.

🔗 Link do Figma: https://www.figma.com/design/awVF8MJKX1rOrNsr8UOwYl/Desafio-Rel%C3%A2mpago

O Figma foi utilizado como guia visual para cores, hierarquia de elementos e posicionamento geral. A versão mobile não foi desenhada no Figma, sendo interpretada diretamente durante a implementação em CSS.

### 🧱 Estrutura do projeto

O projeto foi organizado de forma clara e modular:

## Estrutura do projeto

<details>
<summary>Abrir</summary>

```text
Desafio-Relâmpago-01/
├── index.html              # Página principal (menu)
├── README.md               # Documentação
├── src/                    # Estilos globais
│   ├── base.css
│   ├── layout.css
│   └── animations.css
├── Imagens/                # Assets da Home
│   ├── background.png
│   ├── bloco.png
│   ├── will.png
│   └── agua.png
└── Projetos/               # Projetos do desafio
    ├── MegaManX/
    │   ├── index.html
    │   ├── style.css
    │   └── assets/
    ├── SMW/
    │   ├── index.html
    │   ├── style.css
    │   └── assets/
    └── MK-II/
        ├── index.html
        ├── style.css
        └── assets/
```

</details>

Essa separação facilita a manutenção, leitura do código e futuras expansões do projeto.

---

## 🕹️ Os Projetos Integrados

Como parte do desafio de "encorpar" o portfólio, desenvolvi três mini-projetos temáticos baseados em jogos clássicos. O objetivo foi explorar diferentes técnicas de CSS avançado sem depender de JavaScript.

### 1. Mega Man X (System Check)
**Local:** `/Projetos/MegaManX/`

Uma cena animada que recria a introdução do jogo.

- **Técnicas usadas:**
  - **CSS Animation (`@keyframes`):** Utilizado para criar o disparo do "Buster Shot", movendo um elemento div da esquerda para a direita alterando opacidade e tamanho.
  - **Clip-path:** Para criar as bordas chanfradas futuristas no painel de HUD, fugindo do quadrado padrão.
  - **Linear Gradients:** Para criar o brilho do tiro sem usar imagens.

### 2. Super Mario World (Map Select)
**Local:** `/Projetos/SMW/`

Um mapa de seleção de fases interativo.

- **Técnicas usadas:**
  - **Pixel Art Font:** Integração com Google Fonts para tipografia 8-bit.
  - **CSS Parallax:** Uso de `background-attachment: fixed` para fixar o cenário enquanto o conteúdo rola.
  - **Selector `:target`:** A mágica sem JS! Ao clicar no número da fase (link âncora), o CSS detecta o ID alvo e muda o `display` da caixa de texto correspondente de `none` para `block`.

### 3. Mortal Kombat II (Select Your Fighter)
**Local:** `/Projetos/MK II/`

O projeto mais complexo, recriando a tela de seleção de personagens.

- **Técnicas usadas:**
  - **Radio Button Hack:** O controle total da tela é feito através de inputs do tipo `radio` invisíveis. Ao clicar num personagem (label), marcamos o input correspondente.
  - **Sibling Selectors (`~` e `+`):** O CSS verifica qual input está marcado e altera o estilo do Grid (borda vermelha) e exibe o Modal correspondente.
  - **CSS Grid Areas:** Mapeamento visual para posicionar os botões invisíveis exatamente sobre os rostos na imagem de fundo.
  - **Object-fit:** Para garantir que os sprites dos personagens se ajustem dentro das células sem distorção.

---

## 🎯 CSS e estilização Global

O CSS da página principal foi dividido em três arquivos com responsabilidades bem definidas:

#### `base.css`
- Reset de estilos
- Definição da fonte principal
- Paleta de cores reutilizável
- Estilos globais

#### `layout.css`
- Estrutura da página
- Posicionamento dos elementos
- Organização visual
- Responsividade com media queries

#### `animations.css`
- Animações em CSS puro
- Efeito de “jiggle” no título
- Animação sutil no bloco de mensagem
- Efeito de hover no menu

Todas as animações respeitam a preferência do usuário através de `prefers-reduced-motion`, garantindo melhor acessibilidade.

### 📱 Responsividade

Apesar do protótipo inicial ter sido criado apenas para desktop, o layout foi adaptado manualmente para diferentes tamanhos de tela utilizando:

- Unidades flexíveis
- `flexbox`
- Media queries para largura e altura
- Controle de overflow horizontal

O objetivo foi manter a identidade visual sem comprometer a usabilidade em dispositivos móveis.

### 🧩 Interações especiais

- **Bloco de mensagem:** ao clicar, exibe uma caixa com texto e imagem
- **Easter egg escondido:** uma área invisível que revela uma mensagem surpresa
- Todas as interações são feitas com CSS puro, sem JavaScript

---

## 2. Projeto: Mega Man X

<details> 
<summary>Index.html</summary>

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mega Man X — System Check</title>
  <link rel="preconnect" href="[https://fonts.googleapis.com](https://fonts.googleapis.com)">
  <link rel="preconnect" href="[https://fonts.gstatic.com](https://fonts.gstatic.com)" crossorigin>
  <link href="[https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap](https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap)" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="scanlines"></div>
<main class="stage-container">
    <section class="game-scene">
        <div class="player-group">
            <img src="mega.png" alt="Mega Man X em posição de tiro" class="x-sprite">
            <div class="buster-shot" aria-hidden="true"></div>
        </div>
        <div class="hud-panel">
            <h1 class="hud-title">SYSTEM STATUS: <span class="status-ok">ONLINE</span></h1>
            <ul class="hud-data">
                <li>X-Buster: <span class="charge-level">CHARGING...</span></li>
                <li>Armor: LEVEL 1</li>
                <li>Target: MAVERICK DETECTED</li>
            </ul>
        </div>
    </section>
</main>
</body>
</html>

```

</details>

<details> 
<summary>Style.css</summary>

```css

:root {
  --mmx-blue-dark: #000050;
  --mmx-blue-neon: #00FFFF;
  --mmx-text-white: #ffffff;
  --mmx-alert-red: #ff3333;
  --mmx-ok-green: #33ff33;
  --floor-height-desktop: 33vh; 
  --floor-height-mobile: 33vh;  
}
html, body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    overflow: hidden;
    overscroll-behavior: none;
    background-color: var(--mmx-blue-dark);
    font-family: 'Orbitron', sans-serif;
}
body {
    position: fixed;
    top: 0;
    left: 0;
}
body::before {
    content: "";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    z-index: -1;
    background-image: url('background.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center bottom;
    pointer-events: none;
}
.scanlines {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: repeating-linear-gradient(to bottom, transparent 0px, transparent 2px, rgba(0, 0, 0, 0.3) 3px, rgba(0, 0, 0, 0.3) 4px);
    pointer-events: none;
    z-index: 99;
}
.stage-container {
    width: 100%;
    height: 100%;
    position: relative;
}
.player-group {
    position: absolute;
    z-index: 10;
    height: 25vh; 
    max-height: 450px;
    width: auto; 
    display: inline-block;
    left: 5%; 
    bottom: var(--floor-height-desktop);
}
.x-sprite {
    height: 100%;
    width: auto;
    display: block;
    image-rendering: pixelated;
}
.buster-shot {
    position: absolute;
    z-index: 9;
    background: linear-gradient(to right, var(--mmx-blue-neon), white);
    border-radius: 10px;
    box-shadow: 0 0 15px var(--mmx-blue-neon);
    opacity: 0;
    animation: fireBuster 2s infinite ease-out;
    top: 36%;
    left: 65%;
    height: 6%;
}
@keyframes fireBuster {
    0% { left: 65%; opacity: 1; width: 5%; }
    10% { width: 40%; } 
    60% { opacity: 1; }
    100% { left: 200%; opacity: 0; } 
}
.hud-panel {
    position: absolute;
    top: 5vh;
    right: 5vh;
    width: 22vw;
    min-width: 300px;
    background: rgba(0, 10, 40, 0.9);
    border: 0.2vw solid var(--mmx-blue-neon);
    padding: 1.5vw;
    clip-path: polygon(10% 0, 100% 0, 100% 90%, 90% 100%, 0 100%, 0 10%);
    box-shadow: 0 0 20px rgba(0, 255, 255, 0.2);
    backdrop-filter: blur(4px);
    color: #ffffff;
}
.hud-title {
    font-size: 1.6vw;
    margin: 0 0 1vw 0;
    border-bottom: 0.1vw solid var(--mmx-blue-neon);
    padding-bottom: 0.5vw;
    letter-spacing: 1px;
    color: var(--mmx-blue-neon);
    text-shadow: 0 0 5px rgba(0, 255, 255, 0.5);
}
.hud-data {
    list-style: none; padding: 0; margin: 0;
    font-size: 1.1vw;
    text-shadow: 1px 1px 0 #000;
}
.hud-data li { margin-bottom: 0.5vw; font-family: monospace; }
.status-ok { color: var(--mmx-ok-green); text-shadow: 0 0 5px var(--mmx-ok-green); }
.charge-level { color: var(--mmx-alert-red); animation: blinkAlert 1s infinite alternate; }
@keyframes blinkAlert {
    from { opacity: 0.6; }
    to { opacity: 1; text-shadow: 0 0 8px var(--mmx-alert-red); }
}
@media (max-aspect-ratio: 1/1) {
    .player-group {
        height: 15vh; 
        max-height: none;
        left: 50%;
        transform: translateX(-50%);
        bottom: var(--floor-height-mobile); 
    }
    .buster-shot {
        top: 38%; 
    }
    .hud-panel {
        top: 5vh; 
        right: auto;
        left: 50%;
        transform: translateX(-50%);
        width: 90vw; 
        padding: 15px;
        border-width: 2px;
    }
    .hud-title { 
        font-size: 1.2rem; 
        margin-bottom: 15px;
        border-bottom-width: 1px;
    } 
    .hud-data { font-size: 0.9rem; }
}

```

</details>

---

## 3. Projeto: Super Mario World
<details> 
<summary>Index.html</summary>

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Super Mario World — Map</title>
  <link rel="preconnect" href="[https://fonts.googleapis.com](https://fonts.googleapis.com)">
  <link rel="preconnect" href="[https://fonts.gstatic.com](https://fonts.gstatic.com)" crossorigin>
  <link href="[https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap](https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap)" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
<main class="map-container">
  <h1 class="game-title">Super Mario World</h1>
  <div class="map-frame">
    <nav class="levels">
      <a href="#fase1" class="level-node" aria-label="Nível 1">1</a>
      <span class="path-line"></span>
      <a href="#fase2" class="level-node" aria-label="Nível 2">2</a>
      <span class="path-line"></span>
      <a href="#fase3" class="level-node" aria-label="Nível 3">3</a>
    </nav>
    <section class="info-display">
      <p class="hint-text">Selecione uma fase...</p>
      <article id="fase1" class="panel">
        <h2>A estreia do Yoshi</h2>
        <p>O Yoshi foi criado especialmente para esse jogo, mas a ideia de montá-lo já existia desde os primeiros Marios.</p>
      </article>
      <article id="fase2" class="panel">
        <h2>Segredos no design das fases</h2>
        <p>O jogo usa cores e formas diferentes nos blocos para indicar caminhos secretos de forma sutil.</p>
      </article>
      <article id="fase3" class="panel">
        <h2>A misteriosa Special Zone</h2>
        <p>Existe uma fase chamada Special Zone que muda o visual de vários inimigos depois de completada.</p>
      </article>
    </section>
  </div>
</main>
</body>
</html>

```

</details>

<details> 
<summary>Style.css</summary>

```css

:root {
  --smw-sky: #5C94FC; 
  --smw-coin-yellow: #F8D878;
  --smw-ui-black: #000000;
  --smw-ui-white: #FFFFFF;
}
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: 'Press Start 2P', cursive;
  background-color: var(--smw-sky);
  background-image: url('background.png');
  background-repeat: no-repeat;
  background-position: center bottom;
  background-size: 100% 100%;
  background-attachment: fixed;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  color: var(--smw-ui-white);
  overflow: hidden;
}
.map-container {
  width: 600px;
  max-width: 90vw;
  text-align: center;
  transform-origin: center center;
}
.game-title {
  font-size: 1.5rem;
  color: #FFDE00;
  text-shadow: 3px 3px 0 #000, 1px 1px 0 #000;
  margin-bottom: 2rem;
  line-height: 1.5;
}
.map-frame {
  background-color: rgba(0, 0, 0, 0.7);
  border: 4px solid var(--smw-ui-black);
  border-radius: 8px;
  padding: 30px;
  box-shadow: inset 0 0 0 4px var(--smw-ui-white), 8px 8px 0px rgba(0,0,0,0.5);
  position: relative;
  backdrop-filter: blur(2px);
}
.levels {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 40px;
  position: relative;
}
.path-line {
  flex-grow: 1;
  height: 4px;
  background-image: linear-gradient(to right, var(--smw-ui-white) 50%, transparent 50%);
  background-size: 10px 100%;
  opacity: 0.5;
}
.level-node {
  width: 40px;
  height: 40px;
  background-color: var(--smw-coin-yellow);
  color: var(--smw-ui-black);
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  border: 2px solid var(--smw-ui-black);
  border-radius: 4px; 
  transition: transform 0.1s;
  box-shadow: inset -2px -2px 0 rgba(0,0,0,0.2);
  z-index: 2;
}
.level-node:hover, .level-node:focus {
  transform: scale(1.2);
  background-color: #FFF;
  outline: none;
  cursor: pointer;
}
.info-display { position: relative; min-height: 150px; }
.hint-text {
  position: absolute; width: 100%; top: 30%;
  text-align: center; font-size: 0.8rem; opacity: 0.8;
  text-shadow: 2px 2px 0 #000;
}
.panel {
  display: none;
  background-color: var(--smw-ui-black);
  color: var(--smw-ui-white);
  padding: 20px;
  border: 4px solid var(--smw-ui-white);
  border-radius: 8px;
  box-shadow: 4px 4px 0 #000;
  text-align: left;
  animation: popIn 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.panel:target { display: block; position: relative; z-index: 10; }
.info-display:has(.panel:target) .hint-text { display: none; }
.panel h2 {
  font-size: 14px; margin-top: 0; margin-bottom: 15px;
  color: var(--smw-coin-yellow); text-transform: uppercase; letter-spacing: 1px;
}
.panel p { font-size: 10px; line-height: 1.8; margin: 0; }
@keyframes popIn {
  from { transform: scale(0.8); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}
@media (min-width: 1440px) { .map-container { transform: scale(1.5); } }
@media (min-width: 2560px) { .map-container { transform: scale(2.5); } }
@media (min-width: 3840px) { .map-container { transform: scale(3.5); } }
@media (max-width: 600px) {
    body {
        background-size: auto 100%;
        background-position: center bottom;
    }
    .map-container { width: 95%; transform: scale(1); }
    .map-frame { padding: 15px; }
    .level-node { width: 32px; height: 32px; }
}

```

</details>

---

## 4. Projeto: Mortal Kombat II

<details> 
<summary>Index.html</summary>

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mortal Kombat II - Select Screen</title>
  <link rel="preconnect" href="[https://fonts.googleapis.com](https://fonts.googleapis.com)">
  <link href="[https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap](https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap)" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
<main class="arcade-cabinet">
  <h1 class="main-title">SELECT YOUR FIGHTER</h1>
  <input type="radio" name="char" id="close-modal" checked>
  <input type="radio" name="char" id="sel-subzero">
  <input type="radio" name="char" id="sel-scorpion">
  <input type="radio" name="char" id="sel-liukang">
  <input type="radio" name="char" id="sel-jax">
  <input type="radio" name="char" id="sel-reptile">
  <input type="radio" name="char" id="sel-raiden">
  <input type="radio" name="char" id="sel-kitana">
  <input type="radio" name="char" id="sel-cage">
  <input type="radio" name="char" id="sel-kunglao">
  <input type="radio" name="char" id="sel-shang">
  <input type="radio" name="char" id="sel-mileena">
  <input type="radio" name="char" id="sel-baraka">
  <div class="grid-container">
    <div class="character-grid">
      <label for="sel-subzero" class="char-cell" title="Sub-Zero"><img src="sprites/Sub-Zero.png" alt="Sub-Zero"></label>
      <label for="sel-scorpion" class="char-cell" title="Scorpion"><img src="sprites/Scorpion.png" alt="Scorpion"></label>
      <label for="sel-liukang" class="char-cell" title="Liu Kang"><img src="sprites/Liu Kang.png" alt="Liu Kang"></label>
      <label for="sel-jax" class="char-cell" title="Jax"><img src="sprites/Jax.png" alt="Jax"></label>
      <label for="sel-reptile" class="char-cell" title="Reptile"><img src="sprites/Reptile.png" alt="Reptile"></label>
      <label for="sel-raiden" class="char-cell" title="Raiden"><img src="sprites/Raiden.png" alt="Raiden"></label>
      <label for="sel-kitana" class="char-cell" title="Kitana"><img src="sprites/Kitana.png" alt="Kitana"></label>
      <label for="sel-cage" class="char-cell" title="Johnny Cage"><img src="sprites/Johnny Cage.png" alt="Johnny Cage"></label>
      <label for="sel-kunglao" class="char-cell" title="Kung Lao"><img src="sprites/Kung Lao.png" alt="Kung Lao"></label>
      <label for="sel-shang" class="char-cell" title="Shang Tsung"><img src="sprites/Shang Tsung.png" alt="Shang Tsung"></label>
      <label for="sel-mileena" class="char-cell" title="Mileena"><img src="sprites/Mileena.png" alt="Mileena"></label>
      <label for="sel-baraka" class="char-cell" title="Baraka"><img src="sprites/Baraka.png" alt="Baraka"></label>
    </div>
  </div>
  <div class="modal-overlay">
    <label for="close-modal" class="modal-backdrop"></label>
    <div class="modal-content">
      <label for="close-modal" class="close-btn">X</label>
      <article class="bio-text bio-subzero">
        <h2>SUB-ZERO</h2>
        <p>Dado como morto no Torneio Shaolin, Sub-Zero retorna misteriosamente. Acredita-se que ele viajou para o Outworld para tentar assassinar Shang Tsung mais uma vez. Para isso, ele deve abrir caminho lutando através do torneio de Shao Kahn.</p>
      </article>
      <article class="bio-text bio-scorpion">
        <h2>SCORPION</h2>
        <p>O espectro gerado no inferno emerge das profundezas. Ao saber do retorno de Sub-Zero, ele volta a perseguir o ninja assassino — seguindo-o até o reino sombrio de Outworld, onde continua sua própria missão profana.</p>
      </article>
      <article class="bio-text bio-liukang">
        <h2>LIU KANG</h2>
        <p>Após vencer o Torneio Shaolin e escapar das garras de Shang Tsung, Kang retorna aos seus templos. Ele descobre seu lar sagrado em ruínas e seus irmãos Shaolin mortos em uma batalha cruel contra uma horda de guerreiros de Outworld. Agora, ele viaja para o reino sombrio em busca de vingança.</p>
      </article>
      <article class="bio-text bio-jax">
        <h2>MAJOR JAX</h2>
        <p>Seu nome verdadeiro é Maj. Jackson Briggs, líder de uma unidade de elite das Forças Especiais dos EUA. Após receber um sinal de socorro da Tenente Sonya Blade, Jax embarca em uma missão de resgate. Uma missão que o leva a um mundo macabro onde ele acredita que Sonya ainda está viva.</p>
      </article>
      <article class="bio-text bio-reptile">
        <h2>REPTILE</h2>
        <p>Como protetor pessoal de Shang Tsung, o esquivo Reptile espreita nas sombras, detendo todos aqueles que tentam ferir seu mestre. Acredita-se que sua forma humana seja um disfarce para uma horrenda criatura reptiliana, cuja raça pensava-se estar extinta há milhões de anos.</p>
      </article>
      <article class="bio-text bio-raiden">
        <h2>RAIDEN</h2>
        <p>Observando os eventos se desenrolarem lá do alto, o deus do trovão percebe as intenções sombrias de Shao Kahn. Após alertar os membros remanescentes do Torneio Shaolin, Raiden desaparece repentinamente. Acredita-se que ele tenha se aventurado sozinho em Outworld.</p>
      </article>
      <article class="bio-text bio-kitana">
        <h2>KITANA</h2>
        <p>Sua beleza esconde seu verdadeiro papel como assassina pessoal de Shao Kahn. Vista conversando com um guerreiro do reino da Terra, seus motivos tornaram-se suspeitos para sua irmã gêmea, Mileena. Mas apenas Kitana conhece suas verdadeiras intenções.</p>
      </article>
      <article class="bio-text bio-cage">
        <h2>JOHNNY CAGE</h2>
        <p>Após o torneio de Shang Tsung, o astro das artes marciais desaparece. Ele segue Liu Kang até o Outworld. Lá, ele competirá em um torneio sádico que detém o equilíbrio da existência da Terra — além de servir como roteiro para outro filme de sucesso.</p>
      </article>
      <article class="bio-text bio-kunglao">
        <h2>KUNG LAO</h2>
        <p>Ex-monge Shaolin e membro da Sociedade Lótus Branca, ele é o último descendente do Grande Kung Lao, que foi derrotado por Goro há 500 anos. Percebendo o perigo da ameaça de Outworld, ele se une a Liu Kang para entrar na competição de Shao Kahn.</p>
      </article>
      <article class="bio-text bio-shang">
        <h2>SHANG TSUNG</h2>
        <p>Após perder o controle do Torneio Shaolin, Tsung promete ao seu governante, Shao Kahn, moldar eventos que atrairão os guerreiros da Terra para competir em seu próprio torneio. Convencido por este plano, Shao Kahn restaura a juventude de Tsung e permite que ele viva.</p>
      </article>
      <article class="bio-text bio-mileena">
        <h2>MILEENA</h2>
        <p>Atuando como assassina ao lado de sua irmã gêmea Kitana, a aparência deslumbrante de Mileena esconde suas intenções hediondas. A pedido de Shao Kahn, ela é encarregada de vigiar a suspeita de traição de sua gêmea. Ela deve colocar um fim nisso a qualquer custo.</p>
      </article>
      <article class="bio-text bio-baraka">
        <h2>BARAKA</h2>
        <p>Ele liderou o ataque contra o Templo Shaolin de Liu Kang. Baraka pertence a uma raça nômade de mutantes que vivem nas terras devastadas de Outworld. Suas habilidades de luta chamaram a atenção de Shao Kahn, que o recrutou para o seu exército.</p>
      </article>
    </div>
  </div>
</main>
</body>
</html>

```

</details>

<details> 
<summary>Style.css</summary>

```css

:root {
  --mk-red: #ff0000;
  --mk-gold: #e5c100;
  --mk-dark: #050505;
}
* { box-sizing: border-box; }
body {
  margin: 0;
  height: 100vh;
  background-color: var(--mk-dark);
  background-image: url('background.png');
  background-size: cover;
  background-position: center bottom;
  background-attachment: fixed;
  font-family: 'Press Start 2P', cursive;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
body::after {
  content: " ";
  display: block;
  position: absolute;
  top: 0; left: 0; bottom: 0; right: 0;
  background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
  z-index: 5;
  background-size: 100% 2px, 3px 100%;
  pointer-events: none;
}
input[type="radio"] { display: none; }
.arcade-cabinet {
  position: relative;
  z-index: 10;
  width: 100%;
  max-width: 900px;
  text-align: center;
}
.main-title {
  color: var(--mk-gold);
  text-shadow: 4px 4px 0 #000;
  font-size: 1.8rem;
  margin-bottom: 2rem;
  letter-spacing: 2px;
}
.grid-container {
  display: flex;
  justify-content: center;
}
.character-grid {
  width: 700px; 
  height: 500px;
  background: rgba(0, 0, 0, 0.5);
  border: 4px solid #111;
  box-shadow: 0 0 30px #000;
  display: grid;
  grid-template-columns: repeat(4, 1fr); 
  grid-template-rows: repeat(3, 1fr);    
  padding: 15px;
  gap: 15px; 
}
.char-cell {
  cursor: pointer;
  border: 4px solid #444; 
  background: rgba(0, 0, 0, 0.7); 
  display: flex;
  align-items: flex-end; 
  justify-content: center;
  transition: all 0.2s;
  overflow: hidden;
  position: relative;
}
.char-cell img {
  width: 100%;
  height: 95%;
  object-fit: contain; 
  image-rendering: pixelated;
  transition: transform 0.2s;
}
.char-cell:hover {
  border-color: var(--mk-red);
  box-shadow: 0 0 15px var(--mk-red), inset 0 0 10px var(--mk-red);
  z-index: 2;
}
.char-cell:hover img {
  transform: scale(1.1);
}
input[name="char"]:checked + .char-cell {
  border-color: var(--mk-red);
}
.modal-overlay {
  position: fixed;
  top: 0; left: 0; width: 100%; height: 100%;
  z-index: 999;
  display: flex;
  justify-content: center;
  align-items: center;
  visibility: hidden;
  opacity: 0;
  transition: opacity 0.2s;
  pointer-events: none;
}
input[name="char"]:not(#close-modal):checked ~ .modal-overlay {
  visibility: visible;
  opacity: 1;
  pointer-events: auto;
}
.modal-backdrop {
  position: absolute;
  top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.85);
}
.modal-content {
  position: relative;
  width: 90%;
  max-width: 600px;
  background: #1a1a1a;
  border: 4px solid #555;
  box-shadow: 0 0 0 4px #000, 10px 10px 0 #000; 
  padding: 30px;
  color: #fff;
  z-index: 1000;
  transform: scale(0.95);
  transition: transform 0.2s;
}
input[name="char"]:not(#close-modal):checked ~ .modal-overlay .modal-content {
  transform: scale(1);
}
.close-btn {
  position: absolute;
  top: 15px; right: 20px;
  color: #666;
  cursor: pointer;
  font-size: 1.5rem;
}
.close-btn:hover { color: var(--mk-red); }
.bio-text { display: none; }
.bio-text h2 {
  color: var(--mk-gold);
  text-align: center;
  border-bottom: 4px solid #333;
  padding-bottom: 20px;
  margin-top: 0;
  margin-bottom: 25px;
  text-transform: uppercase;
  text-shadow: 3px 3px 0 #000;
  font-size: 1.5rem;
  letter-spacing: 2px;
}
.bio-text p {
  font-size: 0.8rem; 
  line-height: 2;
  color: #ccc;
  text-align: justify;
  margin: 0;
  font-family: monospace; 
}
#sel-subzero:checked ~ .modal-overlay .bio-subzero { display: block; }
#sel-scorpion:checked ~ .modal-overlay .bio-scorpion { display: block; }
#sel-liukang:checked ~ .modal-overlay .bio-liukang { display: block; }
#sel-jax:checked ~ .modal-overlay .bio-jax { display: block; }
#sel-reptile:checked ~ .modal-overlay .bio-reptile { display: block; }
#sel-raiden:checked ~ .modal-overlay .bio-raiden { display: block; }
#sel-kitana:checked ~ .modal-overlay .bio-kitana { display: block; }
#sel-cage:checked ~ .modal-overlay .bio-cage { display: block; }
#sel-kunglao:checked ~ .modal-overlay .bio-kunglao { display: block; }
#sel-shang:checked ~ .modal-overlay .bio-shang { display: block; }
#sel-mileena:checked ~ .modal-overlay .bio-mileena { display: block; }
#sel-baraka:checked ~ .modal-overlay .bio-baraka { display: block; }
@media (max-width: 750px) {
  .character-grid {
    width: 95vw;
    height: auto; 
    aspect-ratio: 4/3;
    gap: 5px;
    padding: 5px;
  }
  .char-cell { border-width: 2px; }
  .main-title { font-size: 1.2rem; }
  .bio-text p { font-size: 0.7rem; line-height: 1.6; }
}

```

</details>

---

### 👤 Autor

**Luis Gustavo Vieira**

Estudante de desenvolvimento web — Alpha Ed/Tech

- **Email:** vieiralg95@gmail.com
- **GitHub:** https://github.com/vieiralg
- **Page:**  https://vieiralg.github.io/Desafio-01/
- **Figma:** https://www.figma.com/design/awVF8MJKX1rOrNsr8UOwYl/Desafio-Rel%C3%A2mpago