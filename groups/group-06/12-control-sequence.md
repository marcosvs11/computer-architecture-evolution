# 12. Controle e Sequência de Operações

> **Rascunho de planejamento interno — não submeter assim.** Este arquivo organiza a pesquisa e a divisão inicial do trabalho. Substituam as instruções e os campos de responsável por texto final, revisado e referenciado antes do Pull Request.

## Orientação comum

A pesquisa deve explicar o controle e a sequência de operações em termos gerais, relacionados à organização Harvard clássica. Harvard separa os espaços e caminhos de instruções e dados, mas não determina, por si só, uma Unidade de Controle específica, uma ISA, o número de ciclos, o tipo de clock nem um método único para desvios.

O fluxo `Fetch → Decode → Execute → Write Back` só deve aparecer se for identificado como um modelo didático adequado ao exemplo, e não como regra universal. A simultaneidade entre busca de instruções e acesso a dados depende da implementação.

Cada integrante fica responsável por uma seção principal, com texto breve e focado, pelo menos uma fonte confiável e referência registrada em `references.md`. Todos devem revisar a seção de outro integrante antes da consolidação. O exemplo e a representação visual ficam com Marcos, conforme a divisão combinada. Escrevam sem atribuir à Harvard características de um processador específico.

## 12.1 Início da Operação e Participação Humana

**Responsável: Guilherme Henrique Rezende Gonçalves**

**Função da seção:** explicar como uma tarefa pode ser iniciada e em que momento uma pessoa participa do processo.

Pesquisar como um programa, comando, entrada ou evento externo pode dar início a uma tarefa em um sistema computacional. Distinguir a participação humana no nível da tarefa — por exemplo, solicitar uma operação ou fornecer dados — do controle interno contínuo feito pelo processador. Não afirmar que uma pessoa coordena cada ciclo de instrução, nem presumir um mecanismo específico de inicialização para todos os sistemas.

**Entrega individual:** texto breve e focado, com pelo menos uma fonte confiável e referência registrada em `references.md`.

## 12.2 Busca da Instrução e Escolha da Próxima Operação

**Responsável: João Pedro dos Santos Barcelos**

**Função da seção:** apresentar como o processador obtém uma instrução e como a sequência pode avançar.

Explicar, em um modelo geral, o papel do endereço da próxima instrução e da memória de instruções. Descrever o avanço sequencial esperado quando não há mudança de fluxo e indicar que uma condição ou instrução de desvio pode levar a outro endereço. Se usar o termo contador de programa (PC), defini-lo e deixar claro que esse nome e os detalhes de atualização pertencem ao modelo de processador descrito, não à definição de Harvard.

**Entrega individual:** texto breve e focado, com pelo menos uma fonte confiável e referência registrada em `references.md`.

## 12.3 Mecanismos de Controle

**Responsável: Otávio Souza Santos**

**Função da seção:** explicar como o processador coordena as unidades para realizar uma operação.

Pesquisar o papel funcional da Unidade de Controle na interpretação da instrução e na coordenação de ações, como selecionar operandos, orientar uma operação da ULA e indicar leituras ou escritas. Distinguir sinais de controle de caminhos que transportam dados ou instruções. Não definir circuitos, sinais ou fases específicos como obrigatórios em toda implementação Harvard.

**Entrega individual:** texto breve e focado, com pelo menos uma fonte confiável e referência registrada em `references.md`.

## 12.4 Sincronização, Repetições e Mudanças no Fluxo

**Responsável: Renato Santos Kitada**

**Função da seção:** explicar como operações podem se repetir e como a execução pode sair da sequência esperada.

Pesquisar sincronização temporal em processadores síncronos, repetição por laços e mudanças de fluxo por condições ou desvios. Definir clock antes de usá-lo e registrar que sua frequência e seu funcionamento são detalhes da implementação. Explicar desvios de forma conceitual; não presumir registradores de flags, instruções ou regras de desvio de uma ISA específica.

**Entrega individual:** texto breve e focado, com pelo menos uma fonte confiável e referência registrada em `references.md`.

## 12.5 Exemplo de Operação e Representação da Sequência

**Responsável: Marcos Vinicius Vieira de Souza**

**Função da seção:** atender ao exemplo obrigatório da Issue e tornar a ordem das etapas fácil de acompanhar.

Usar uma operação didática, como somar dois valores e guardar o resultado. Apresentar a sequência do início ao resultado, identificando quando ocorre busca da instrução, interpretação, obtenção dos operandos, cálculo e armazenamento. Se usar uma notação como `R ← A + B`, identificá-la como pseudocódigo, não como instrução de uma ISA real. Produzir uma representação visual simples da sequência e incluir legenda. Não garantir acessos simultâneos nem fixar a quantidade de ciclos.

**Entrega individual:** exemplo passo a passo, representação visual com legenda, fonte(s) que sustentem a explicação e referências registradas em `references.md`.

## 12.6 Condições de Encerramento

**Responsável: Victor Francisco Rodrigues Pereira Melo**

**Função da seção:** explicar quando a operação ou tarefa considerada termina.

Pesquisar como reconhecer a conclusão de uma operação ou tarefa em termos gerais, distinguindo o término de uma instrução, de uma tarefa e do programa. Explicar que, depois de uma operação, o processador pode prosseguir para outra instrução, aguardar ou encerrar a execução conforme o sistema e a implementação. Não apresentar um mecanismo de encerramento específico como obrigatório em toda Arquitetura Harvard.

**Entrega individual:** texto breve e focado, com pelo menos uma fonte confiável e referência registrada em `references.md`.

## Revisão entre integrantes

Antes de consolidar, cada integrante deve revisar a seção de outra pessoa: conferir clareza, coerência com a Harvard clássica, afirmações sustentadas por fontes e referências registradas. A revisão é compartilhada; não fica sob responsabilidade exclusiva de uma pessoa.

## Referências da entrega

As fontes usadas por todos os integrantes devem ser incluídas em `references.md`, no padrão adotado pelo grupo. Cada integrante deve enviar a referência completa e informar qual afirmação ou parte do texto ela sustenta.
