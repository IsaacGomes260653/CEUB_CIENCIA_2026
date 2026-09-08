# PlayHub — Portal de Mini-Jogos

Portal de mini-jogos gratuitos, direto no navegador. HTML, CSS e JavaScript puros — sem frameworks, sem build, sem instalação. Também funciona como PWA (instalável e com suporte offline via Service Worker).

## Jogos

| Jogo | Descrição |
|---|---|
| 🎮 Jogo da Velha | Clássico 2 jogadores no mesmo dispositivo |
| 🐍 Snake | Coma as maçãs, cresça e não bata na parede nem em você mesmo |
| 🔢 2048 | Combine os números e tente chegar ao bloco 2048 |
| 🃏 Jogo da Memória | Vire as cartas e encontre todos os pares |
| 🧩 Quebra-Cabeça 15 | Reorganize as peças até formar a sequência correta |
| 💣 Campo Minado | Revele as células sem tocar em nenhuma mina, três níveis |
| ⚽ Fantasy World Cup | Monte seu Dream Team escalando jogadores reais de Copas do Mundo históricas por posição no campo (com formações táticas: 4-4-2, 4-3-3, 3-5-2, 5-3-2, 4-2-3-1) e dispute um torneio simulado |

## Rodando localmente

Como é um site 100% estático, basta servir a pasta com qualquer servidor HTTP simples (necessário para o Service Worker/PWA funcionar corretamente — abrir os arquivos direto via `file://` também funciona para jogar, mas sem PWA):

```bash
# Python
python -m http.server 8080

# ou Node
npx serve .
```

Depois acesse `http://localhost:8080`.

## Estrutura do projeto

```
.
├── index.html          # Página inicial com a grade de jogos
├── about.html           # Sobre o projeto
├── manifest.json         # Manifest do PWA
├── sw.js                 # Service Worker (cache offline)
├── assets/
│   ├── style.css          # Estilo global (temas, layout, componentes)
│   ├── theme.js           # Alternância de temas
│   ├── sfx.js              # Efeitos sonoros
│   ├── share.js            # Compartilhamento de resultados
│   ├── pwa.js               # Registro do Service Worker / instalação PWA
│   ├── icons.js              # Ícones SVG inline usados nos jogos
│   ├── photos.js              # Utilitários de imagens/fotos
│   └── icon.svg                 # Ícone do app
└── games/
    ├── tictactoe.html
    ├── snake.html
    ├── 2048.html
    ├── memory.html
    ├── puzzle.html
    ├── minesweeper.html
    └── worldcup.html
```

## Tecnologias

- HTML5, CSS3, JavaScript (vanilla, sem dependências externas)
- PWA (manifest + service worker) para instalação e uso offline
- Alternância de tema visual (Retro/Neon) via `assets/theme.js`

## Aulas (Desenvolvimento Web — UniCEUB)

Além do PlayHub, o repositório guarda os exercícios da disciplina de Desenvolvimento Web:

| Pasta | Conteúdo |
|---|---|
| `Aula02/` | Formulário, lista e tabela em HTML puro (tags básicas, sem CSS) |
| `Aula03/` | Formulário "Escola Virtual" com CSS embutido no `<head>` |
| `Aula04/` | Formulário "Escola Virtual" evoluído: CSS em arquivo separado, máscaras de CPF/telefone/CEP, preenchimento automático de endereço via API ViaCEP, cálculo de idade e campos condicionais por série |

## Licença

Uso pessoal / educacional.

---

# PlayHub — Mini-Games Portal (English)

A free mini-games portal that runs straight in the browser. Pure HTML, CSS, and JavaScript — no frameworks, no build step, no install. Also works as a PWA (installable, with offline support via Service Worker).

## Games

| Game | Description |
|---|---|
| 🎮 Tic-Tac-Toe | Classic 2-player, same device |
| 🐍 Snake | Eat the apples, grow, don't hit the wall or yourself |
| 🔢 2048 | Merge the numbers and try to reach the 2048 tile |
| 🃏 Memory | Flip the cards and find all the pairs |
| 🧩 15 Puzzle | Rearrange the tiles until they're in order |
| 💣 Minesweeper | Clear the board without hitting a mine, three difficulty levels |
| ⚽ Fantasy World Cup | Build your Dream Team from real players across historic World Cups, by field position (tactical formations: 4-4-2, 4-3-3, 3-5-2, 5-3-2, 4-2-3-1), and play a simulated tournament |

## Running locally

Since it's a fully static site, just serve the folder with any simple HTTP server (needed for the Service Worker/PWA to work correctly — opening the files directly via `file://` also works for playing, just without PWA support):

```bash
# Python
python -m http.server 8080

# or Node
npx serve .
```

Then open `http://localhost:8080`.

## Tech stack

- HTML5, CSS3, JavaScript (vanilla, no external dependencies)
- PWA (manifest + service worker) for install and offline use
- Visual theme switcher (Retro/Neon) via `assets/theme.js`

## Classes (Web Development — UniCEUB)

Besides PlayHub, the repository also holds the exercises from the Web Development course:

| Folder | Content |
|---|---|
| `Aula02/` | Form, list, and table in plain HTML (basic tags, no CSS) |
| `Aula03/` | "Virtual School" form with CSS embedded in the `<head>` |
| `Aula04/` | "Virtual School" form, evolved: CSS in its own file, CPF/phone/ZIP masks, automatic address lookup via the ViaCEP API, age calculation, and grade-conditional fields |

## License

Personal / educational use.
