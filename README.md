# Nexus Cores
 
PROJ02
### Perguntas para Reflexão

1. **Compreensão do Fluxo do Jogo:**
   - Como o fluxo do jogo se desenrola desde o início até a verificação da entrada do usuário?
   - R: Fluxo do Jogo: O jogo começa quando o jogador clica no botão "Iniciar Jogo", acionando a função generateSequence. A sequência de cores é exibida, e, após a exibição, o jogador deve repetir a sequência ao clicar nas cores. A função checkInput verifica se a     
     sequência clicada está correta.
     Verificação da Entrada: A cada clique do usuário, checkInput compara a sequência do jogador com a sequência do jogo. Se o jogador acerta, uma nova sequência é gerada, aumentando o nível; caso contrário, o jogo é reiniciado.

2. **Lógica da Sequência:**
   - Como a sequência de cores é gerada e exibida ao jogador?
   - R: Geração da Sequência: A função generateSequence adiciona uma cor aleatória à sequência existente, escolhendo-a com Math.random() a partir do array colors.
     Exibição da Sequência: A função displaySequence usa setInterval para destacar cada cor da sequência, chamando highlightColor com um intervalo de 1 segundo para cada cor, indicando a sequência ao jogador de forma visual.

3. **Uso de Funções:**
   - As funções estão organizadas de forma clara? O que você faria diferente?
   - R: As funções estão organizadas de forma lógica, seria interessante separar a lógica de sequência da lógica de exibição. Além disso, agrupar funções relacionadas (como highlightColor e displaySequence) em um objeto ou classe ajudaria na legibilidade e manutenção.

4. **Manipulação do DOM:**
   - Como o código utiliza a manipulação do DOM para atualizar a interface?
   - R: O código manipula o DOM para atualizar a interface de várias maneiras. Por exemplo, messageDisplay.textContent exibe mensagens e o método style.opacity modifica a aparência dos elementos de cor.

5. **Interatividade:**
   - Como os eventos de clique são configurados e gerenciados?
   - R:  Os eventos de clique são configurados em enableUserInput, que adiciona ouvintes de clique a cada elemento de cor para registrar a sequência do jogador.
      Cada clique adiciona a cor à sequência do jogador (userInput), que é verificada por checkInput. Para melhorar a experiência, a remoção de eventos após cada rodada pode ser implementada para evitar cliques fora de hora.

6. **Debugging:**
   - Você encontrou erros? Como você os resolveu?
   - R: Durante a implementação, erros comuns poderiam incluir uma comparação incorreta na função checkInput ou elementos null ao tentar referenciar divs de cor antes de o DOM estar completamente carregado. Para resolver, pode-se adicionar verificações de null e garantir que o DOM esteja pronto antes de tentar referenciar elementos.

7. **Extensibilidade:**
   - Que recursos adicionais você gostaria de adicionar ao jogo? Como você abordaria isso?
   - R: Recursos Adicionais: Algumas melhorias incluem adicionar um sistema de pontuação, salvar o nível mais alto, aumentar a velocidade de exibição da sequência em níveis mais avançados, ou adicionar sons para cada cor.
Implementação: A pontuação pode ser incrementada a cada rodada em que o jogador acerta, e exibida no messageDisplay. Para aumentar a velocidade, o intervalo em displaySequence pode ser reduzido conforme o nível sobe.
