<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização com foco no design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Este é um processo de desenvolvimento com foco no design: comece com a visão, refine os elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Digite este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon no título pulsando como um letreiro, selo VS animado com mudanças nas cores do gradiente, sobreposição de brilho e cintilação nos cards de resultado dos usuários, animações de entrada flutuante nos campos, texto de carregamento que muda entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuições. Mantenha o fundo escuro (`#0a0a1a`) com detalhes em verde (`#5fed83`) e roxo (`#8a2be2`). Use um tema escuro com a fonte de jogos retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado de implementação com todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e faça ajustes:

- Sugira ajustes na duração das animações (por exemplo, *"Deixe a pulsação neon mais lenta, em cerca de 3 segundos"*).
- Pergunte sobre efeitos específicos (por exemplo, *"Como vai funcionar a sobreposição de brilho nos cards?"*).
- Peça alterações na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições à folha de estilos. Isso pode incluir:

- `@keyframes` para o efeito de linhas de varredura, o pulso neon, o brilho e as animações de entrada flutuante.
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades personalizadas de CSS para as cores do tema.
- Transições e estados `hover` para elementos interativos.

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador à força (`Ctrl+Shift+R`).

Mantenha a prévia do navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deve pulsar de forma mais intensa.

Este é um processo de **desenvolvimento com foco no design** — você está refinando o resultado visual em tempo real. Cada prompt aprimora a experiência até que ela fique do jeito que você quer. Não se contente com algo "bom o suficiente": refine até a página parecer saída de um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione uma seção de guia de design a copilot-instructions.md descrevendo o tema de fliperama retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um guia de design curto para o tema de fliperama retrô: cores, fontes, estilo das animações e a regra de que a nova interface deve manter a estética neon.
<!-- track:cli:end -->

Faça commit das instruções atualizadas e das alterações de design quando a página estiver como você quer.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para esboçar um **sistema de design antes de implementá-lo**.
- **Iterar no resultado visual** com feedback rápido.
- **Atualizar as instruções depois das principais decisões** para manter a identidade visual.
