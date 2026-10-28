# 8. Integração, Limitações e Desempenho

## 8.1 Integração dos Componentes e Decisões Arquiteturais

## 8.2 Características Favoráveis e Benefícios Condicionais

## 8.3 Comunicação e Paralelismo, Quando Aplicável
Na organização Harvard clássica, as instruções e os dados ocupam espaços de memória separados e utilizam caminhos de comunicação independentes com o processador. Assim, a busca de uma instrução não precisa usar o mesmo caminho empregado por uma leitura ou escrita na memória de dados. Essa organização pode permitir que a busca de instruções e um acesso a dados ocorram de forma sobreposta, desde que a implementação consiga atender às duas operações nesse intervalo.

Essa possibilidade representa independência entre acessos às memórias; não significa, por si só, que duas instruções sejam executadas ao mesmo tempo. A ocorrência e o benefício da sobreposição dependem de fatores da implementação, como a organização das memórias, a capacidade de atender acessos simultâneos, a latência e o controle do processador. Portanto, a separação dos caminhos aumenta o potencial de paralelismo de acesso, mas não garante simultaneidade nem um ganho fixo de desempenho.

A arquitetura Harvard também não implica automaticamente o uso de pipeline. Pipeline é uma escolha de implementação que divide a execução em etapas e permite sobrepor etapas de instruções diferentes. Para isso, são necessários mecanismos próprios de controle e tratamento de dependências. A separação entre os caminhos de instruções e dados pode favorecer essa organização, mas não a determina.

A independência dos caminhos pode reduzir a disputa pelo mesmo caminho de comunicação entre instruções e dados. Ainda assim, não elimina todos os possíveis gargalos: o desempenho continua condicionado à implementação e às operações realizadas.

## 8.4 Desempenho e Capacidade de Processamento

## 8.5 Armazenamento, Limitações e Gargalos
A adoção da organização Harvard acarreta implicações diretas sobre a estrutura de armazenamento e introduz condicionantes específicos de desempenho:

* **Impacto da Separação no Armazenamento:** A divisão física entre os espaços de programa e de dados obriga a que qualquer alteração estrutural no volume de instruções ou na quantidade de variáveis guardadas exija recursos de hardware distintos e dedicados, impedindo a partilha flexível do mesmo bloco de memória física entre código e dados.
* **Limitações do Modelo e Decisões de Implementação:** É essencial distinguir as restrições conceptuais da arquitetura das limitações físicas impostas por uma implementação concreta. Enquanto o modelo Harvard assegura a separação lógica e de caminhos, aspetos como a **capacidade máxima**, a **tecnologia de suporte** (seja fita perfurada eletromecânica, relés ou semicondutores modernos) e a **velocidade de acesso** dependem estritamente das escolhas de projeto de cada sistema.
* **Gargalos Operacionais:** Restrições como o tempo de resposta dos componentes de armazenamento ou a largura de banda dos canais dedicados continuam a influenciar o fluxo de execução. Consequentemente, o desempenho global permanece condicionado pela sincronização entre a velocidade de leitura das instruções e a capacidade de processamento e retenção dos dados nas unidades de cálculo.
## 8.6 Contexto de Uso e Resposta à Questão Central

