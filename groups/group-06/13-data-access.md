# 13. Seleção e Acesso aos Dados

## 13.1 Escopo e Exemplo Adotado

## 13.2 Localização dos Dados e dos Operandos

## 13.3 Identificação e Seleção dos Operandos
No ATmega328P, a instrução indica seus operandos conforme formas definidas pela ISA AVR. Em ADD R16, R17, os valores são identificados pelos registradores especificados na instrução. Em LDI R16, K, K representa uma constante imediata fornecida como operando da instrução. Já em LDS R16, k, k identifica uma posição do espaço de dados cujo conteúdo é carregado em R16. Uma alternativa é o acesso indireto, como em LD R16, X, no qual o endereço do dado é indicado pelo conteúdo do registrador ponteiro X [1], [2].

Esses exemplos mostram maneiras distintas de selecionar operandos nesta ISA: por registrador, por constante e por posição de memória. O endereço identifica onde buscar um valor; ele não deve ser confundido com o próprio valor. Também é necessário distinguir essas formas de endereçamento da organização Harvard: a separação entre os espaços de instruções e dados é uma característica organizacional, enquanto os mnemônicos e operandos apresentados pertencem ao ATmega328P/AVR [1], [2].

## 13.4 Modos de Endereçamento e Mecanismos de Acesso

## 13.5 Exemplo de Seleção e Uso de um Dado

## 13.6 Limitações e Relação com a Organização Harvard

