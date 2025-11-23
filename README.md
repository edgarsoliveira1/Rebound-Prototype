# One Shot, One Room 🎯

> **Status:** Protótipo Jogável (MVP)  
> **Gênero:** Top-Down Action / Puzzle / Stealth

**One Shot, One Room** é um protótipo de jogo tático desenvolvido em HTML5 e JavaScript puro (Vanilla JS). O jogo combina a letalidade rápida de *Hotline Miami* com mecânicas de física e ricochete.

O jogador possui apenas **uma munição**. A bola mágica não recarrega sozinha; ela deve ser recuperada fisicamente após cada disparo, criando um ciclo de tensão constante entre ataque e vulnerabilidade.

---

## 🎮 Como Jogar

O objetivo é sobreviver a ondas de inimigos utilizando o layout das salas a seu favor.

### Controles
| Ação | Input (Teclado/Mouse) |
| :--- | :--- |
| **Mover** | `W`, `A`, `S`, `D` ou Setas |
| **Mirar** | Mouse |
| **Atirar** | Clique Esquerdo (LMB) |
| **Recarregar** | Caminhe até a bola parada para pegá-la |

### Mecânicas Principais
1.  **A Única Bala:** Sua arma é um projétil físico. Se você errar ou a bola parar longe, você estará indefeso até correr e buscá-la.
2.  **Geometria Letal:** A bola ricocheteia nas paredes. Use ângulos ("tabelas") para atingir inimigos em outras salas sem se expor.
3.  **Sistema de Visão (LOS):** Os inimigos usam *Line of Sight*. Eles não te veem através das paredes.
    * 🔴 **Vermelho Escuro:** Patrulha/Inativo (Não te viu).
    * 🚨 **Vermelho Vivo:** Perseguição (Te viu).

---

## 🚀 Como Rodar o Jogo

Este é um projeto *client-side* puro. Não requer instalação (Node, Python, etc).

1.  Baixe o arquivo `index.html` (ou clone este repositório).
2.  Abra o arquivo diretamente em qualquer navegador moderno (Chrome, Firefox, Edge, Brave).
3.  O jogo iniciará automaticamente.

---

## 🔮 Roadmap & Melhorias Futuras

Embora o núcleo mecânico esteja funcional, o plano para transformar este protótipo em um jogo comercial (Steam/Itch.io) inclui as seguintes expansões:

### 1. Visual & "Game Juice" (Polimento)
* [ ] **Iluminação Dinâmica:** Implementar sistema de luz e sombra (Raycasting). Salas não visitadas devem ser escuras (Fog of War), iluminadas apenas pelo rastro da bola.
* [ ] **Feedback Visceral:** Adicionar *Screen Shake* (tremor de tela) em impactos e *Hit Stop* (congelamento de milissegundos) ao eliminar inimigos.
* [ ] **Decals Permanentes:** Inimigos eliminados deixam marcas no chão, contando a história da batalha.

### 2. Design de Inimigos (Arquétipos)
Para forçar novas estratégias além de "correr e atirar":
* [ ] **O Sniper:** Inimigo estacionário com linha de visão longa e tiro hitscan.
* [ ] **O Escudeiro:** Possui blindagem frontal. O jogador é **obrigado** a usar o ricochete na parede para atingi-lo pelas costas.
* [ ] **O Kamikaze:** Explode ao morrer, criando uma zona de perigo temporária que impede o jogador de recuperar a bola imediatamente.

### 3. Meta-Game (Roguelike)
* [ ] **Geração Procedural:** Substituir o mapa fixo por geração aleatória de salas e corredores.
* [ ] **Sistema de Relíquias:** Ao final de cada nível, o jogador escolhe um upgrade:
    * *Ímã:* A bola retorna lentamente ao segurar espaço.
    * *Heavy Ball:* Atravessa o primeiro inimigo e mata o segundo.
    * *Trail Blaze:* A bola deixa um rastro de fogo que causa dano por área.

### 4. Áudio Imersivo
* [ ] **Trilha Sonora Dinâmica:** A música alterna suavemente entre "Baixo/Tensão" (Stealth) e "Bateria/Agressiva" (Combate) dependendo do estado dos inimigos.

### 5. Migração Tecnológica
* [ ] Portar a lógica do JavaScript puro para uma Engine dedicada (**Godot 4** ou **GameMaker**) para garantir performance nativa, suporte a controles (gamepad) e exportação facilitada.

---

## 🛠️ Tecnologias e Algoritmos

Este protótipo foi criado para demonstrar conceitos de Game Design sem dependências externas.

* **Renderização:** HTML5 Canvas API.
* **Colisão:** AABB (Axis-Aligned Bounding Box) para tiles e Circle-Collision para a bola.
* **IA:** Raycasting simples para detecção de paredes entre Inimigo e Jogador.

---

*Projeto criado para fins de estudo de Game Design e Prototipagem Rápida.*