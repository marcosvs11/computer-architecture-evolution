# 13. Seleção e Acesso aos Dados

## 13.1 Escopo e Exemplo Adotado
Um operando é um valor, registrador ou referência a uma posição de memória utilizado por uma instrução durante sua execução. No ATmega328P, os operandos podem ser fornecidos diretamente na instrução, obtidos dos registradores de uso geral ou localizados na memória de dados por meio de endereços. Por exemplo, na instrução ADD R16, R17, os registradores R16 e R17 identificam os valores que serão somados, e o resultado é armazenado em R16. Quando os dados estão na memória, instruções específicas permitem acessá-los por endereçamento direto ou indireto, utilizando registradores como ponteiros para localizar suas posições. Também existem mecanismos para acessar posições específicas da memória de programa, como a Flash, por meio de instruções próprias. Esses recursos mostram como o processador identifica, seleciona e recebe os dados necessários para realizar uma operação. Entretanto, os mecanismos apresentados são características da implementação AVR do ATmega328P, e não regras obrigatórias de toda arquitetura Harvard. O princípio geral de Harvard está na separação entre memória de instruções e memória de dados, enquanto a quantidade de registradores, os modos de endereçamento, as instruções e as formas de acesso dependem de cada processador.

## 13.2 Localização dos Dados e dos Operandos

## 13.3 Identificação e Seleção dos Operandos
No ATmega328P, a instrução indica seus operandos conforme formas definidas pela ISA AVR. Em ADD R16, R17, os valores são identificados pelos registradores especificados na instrução. Em LDI R16, K, K representa uma constante imediata fornecida como operando da instrução. Já em LDS R16, k, k identifica uma posição do espaço de dados cujo conteúdo é carregado em R16. Uma alternativa é o acesso indireto, como em LD R16, X, no qual o endereço do dado é indicado pelo conteúdo do registrador ponteiro X [1], [2].

Esses exemplos mostram maneiras distintas de selecionar operandos nesta ISA: por registrador, por constante e por posição de memória. O endereço identifica onde buscar um valor; ele não deve ser confundido com o próprio valor. Também é necessário distinguir essas formas de endereçamento da organização Harvard: a separação entre os espaços de instruções e dados é uma característica organizacional, enquanto os mnemônicos e operandos apresentados pertencem ao ATmega328P/AVR [1], [2].

## 13.4 Modos de Endereçamento e Mecanismos de Acesso

## 13.5 Exemplo de Seleção e Uso de um Dado

## 13.6 Limitações e Relação com a Organização Harvard

