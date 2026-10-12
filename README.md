# Tennis Pong

**MATCH POINT — 8-Bit Tennis** é um jogo arcade de tênis em pixel art, executado diretamente no navegador. A partida é desenhada em um elemento HTML Canvas e implementada com JavaScript, sem framework ou etapa de compilação.

## Recursos

- Partida individual contra a CPU, com quatro níveis: Iniciante, Defensor, Agressivo e Pro.
- Modo Casual e modo Treino, com a CPU no nível fácil.
- Opção de dois jogadores no mesmo dispositivo.
- Interface em português brasileiro (padrão) e inglês.
- Ciclo visual de dia e noite, animações, efeitos sonoros e replay/demo.
- Estatísticas, histórico de partidas e recordes salvos no armazenamento local do navegador.
- Controles por teclado, toque/deslize e gamepad compatível com a Gamepad API do navegador.

## Como jogar

1. Abra `index.html` em um navegador moderno.
2. Na tela inicial, escolha o modo e, se aplicável, a dificuldade; ative a opção de 2 jogadores se quiser jogar localmente.
3. Selecione **Iniciar**.

### Controles

| Ação | Controle |
|---|---|
| Jogador 1: rebater à esquerda / centro / direita | `←` / `↑` / `→` |
| Jogador 2 no modo local: rebater à esquerda / centro / direita | `A` / `W` / `D` |
| Dispositivo com tela sensível ao toque | Deslize para cima; a direção horizontal do gesto escolhe a rebatida |
| Navegar/confirmar nos menus | Teclas de direção e `Enter` ou espaço |
| Voltar nos menus | `Esc` ou `Backspace` |

O mouse/toque também pode ser usado para interagir com os controles desenhados na tela.

## Executar por servidor local

Também é possível servir os arquivos localmente com Python:

```bash
python3 -m http.server 8000
```

Depois, acesse <http://localhost:8000>.

Não é necessário instalar dependências JavaScript nem executar um processo de build. O jogo não precisa de backend; as estatísticas e configurações ficam no `localStorage` do navegador. A fonte pixelada é carregada do Google Fonts quando há conexão com a internet; sem conexão, o CSS usa uma fonte monoespaçada de fallback.

## Estrutura

```text
.
├── index.html   # estrutura da página e canvas
├── script.js    # lógica, física, renderização, áudio e controles
├── style.css    # layout, escala e efeitos CRT
└── README.md    # documentação do projeto
```

## Verificação

A sintaxe do JavaScript pode ser verificada com:

```bash
node --check script.js
```
