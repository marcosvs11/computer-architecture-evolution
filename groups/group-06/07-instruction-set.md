# 7. Modelo de Operações e Instruções

## 7.1 Harvard e ISA

## 7.2 Como o Programa Chega ao Microcontrolador

## 7.3 Operações e Tipos de Instrução
Para examinar operações reais, esta seção usa como exemplo o microcontrolador ATmega328P, presente na placa Arduino Uno Rev3. As instruções descritas a seguir pertencem à ISA AVR implementada por esse microcontrolador. Elas não são definidas pela Arquitetura Harvard, que descreve uma organização com espaços separados para instruções e dados [1]–[3].

Entre as operações aritméticas do AVR está ADD Rd, Rr. Essa instrução soma os valores dos registradores indicados e grava o resultado no registrador destino Rd. Assim, ela ilustra uma operação realizada pelo processador sobre operandos mantidos em registradores. O manual AVR também descreve os efeitos da operação sobre as flags de estado, que podem ser usadas por instruções posteriores [1].

A transferência de dados aparece em instruções com funções diferentes. MOV Rd, Rr copia um valor de um registrador para outro. Já LD e ST permitem, respectivamente, carregar um valor do espaço de dados para um registrador e armazenar no espaço de dados o valor de um registrador. Essas instruções não devem ser tratadas como equivalentes: MOV transfere entre registradores, enquanto LD e ST envolvem acesso ao espaço de dados.

O AVR também possui instruções de controle de fluxo, como BRNE. Essa instrução realiza um desvio condicional quando a flag Z está zerada. Como a condição depende de uma flag, normalmente uma instrução anterior — por exemplo, uma comparação — precisa ter produzido o estado que será testado. Portanto, BRNE não deve ser descrita como uma instrução que compara diretamente dois operandos.

A instrução LPM permite ler informação armazenada na memória de programa, conforme a forma de uso definida pela ISA AVR. Esse caso ajuda a relacionar o exemplo concreto à separação entre espaços de memória: a existência e a semântica de LPM, porém, são características do AVR estudado e não uma regra universal da Arquitetura Harvard.

As categorias apresentadas são uma seleção de exemplos da ISA AVR, não uma lista completa. A separação Harvard ajuda a descrever onde instruções e dados estão organizados; ela não determina, por si só, quais instruções aritméticas, de transferência ou de desvio um processador deve possuir.

## 7.4 Codificação, Operandos e Endereçamento

## 7.5 Exemplo de Instrução ou Operação

Write a simple Assembly program.

## 7.6 Relação com o Hardware e Limitações

Compare with ARM or x86.
