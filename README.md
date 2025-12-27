# Guia do Projeto: Lyric - So se fu...

## Como o código funciona?
O código usa uma função chamada time.monotonic(). Ela funciona como um cronômetro que começa a contar no momento em que você dá o "play". O programa fica checando esse cronômetro milhares de vezes por segundo para saber se já chegou a hora de mostrar a próxima frase.
Os Comandos ANSI em vez de apenas imprimir texto, o código envia comandos "invisíveis" (chamados ANSI) para o terminal. Eles dizem: "Limpe a tela agora", "Mude a cor para cinza" ou "Mova o cursor para o topo". É isso que permite que a neve caia e as letras mudem de cor sem que o terminal fique cheio de linhas repetidas.
Organizador de Texto (Auto-Wrap): Se você escrever uma frase muito longa, o código tem uma lógica que a "quebra" em várias linhas automaticamente, garantindo que nenhuma palavra seja cortada pela metade na borda da janela. Ou você pode escrever o (\n) entre as frases.

---

### Configurando o VS Code para rodar
Para ver o efeito das cores e das letras mudando, o terminal do VS Code precisa estar configurado corretamente:

#### 1. Preparação
Certifique-se de que a extensão Python da Microsoft está instalada. Abra a pasta do projeto no VS Code.

#### 2. Abrindo o Terminal Correto
Não use o "Console de Depuração". Vá no menu superior em Terminal > Novo Terminal.

### Dica para Windows: No canto do terminal, verifique se está escrito PowerShell ou zsh/bash. O "Prompt de Comando" (CMD) antigo pode não mostrar as cores corretamente.

#### 3. Execução - Clique no botão de Play no canto superior direito ou digite no terminal:

* **`python sose.py`**
---
Como alterar a música e os tempos
No final do arquivo sose.py, você encontrará a lista LYRICS_DATA. Para cada linha, você define:

**"time"**: O momento exato (em segundos) que a frase deve aparecer.

**"original"**: O texto que será exibido.

**"highlight"**: True: Se quiser que aquela frase específica tenha um brilho ou destaque extra.

