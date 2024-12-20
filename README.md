# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

# Questão 1. Introdução a sistemas operacionais

Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos
- Gerenciamento de memória
- Gerenciamento de dispositivos de entrada e saída
- Gerenciamento de arquivos

**Dica**: Pense em exemplos práticos de como o sistema operacional realiza essas tarefas no dia a dia de um usuário.

**Copilot informa**: Essa questão incentiva os alunos a explorarem os conceitos fundamentais e a aplicarem o conhecimento teórico em situações práticas. Se precisar de mais alguma coisa, estou aqui para ajudar!

## Resposta
O sistema operacional (SO) gerencia os recursos de hardware e software de diversas maneiras, para o gerenciamento de processos é possível observar que o sistema tenta dividir de maneira justa a capacidade de processamento pois dependendo da tarefa elas podem monopolizar a CPU fazendo com o que nenhuma outra tarefa seja executada, além disso as prioridades definidas pelo usuário também sao levadas em consideração na hora de dividir o uso da CPU. Já na parte de gerencia de memória o SO fornece a cada aplicaçao uma área de memória própria isolada das demais aplicações e do próprio SO o que melhora a estabilidade e segurança do sistema. Na parte de gerenciamento dos dispositivos de entrada e saida é realizado por meio de um dispositivo denonimado controladores de dispositivos os quais são responsáveis por permitir que o software interaja com o hardware sendo essas interações as seguintes ações: aceitar, executar, desligar. Por fim o gerenciamento de arquivos também é feita pelos controladores de dispositivos visando criar arquivos e diretórios, os dispositivos definem as regras de uso e interface de acesso necessária para o sistema.

# Questão 2. Estrutura de sistemas operacionais

## Texto informativo
### Estrutura de Sistemas Operacionais: Custo de Desenvolvimento e Segurança da Informação

A estrutura de um sistema operacional (SO) é fundamental para determinar tanto o custo de desenvolvimento e manutenção quanto a segurança da informação. Existem várias arquiteturas de SO, como monolítica, microkernel e em camadas, cada uma com suas próprias implicações em termos de custo e segurança.

#### Custo de Desenvolvimento e Manutenção

1. **Arquitetura Monolítica**:
   - **Desenvolvimento**: Geralmente, mais rápida de desenvolver inicialmente, pois todos os componentes do SO são integrados em um único bloco de código.
   - **Manutenção**: Pode ser mais complexa e cara, pois qualquer alteração em um componente pode afetar todo o sistema, exigindo testes extensivos e cuidadosos.

2. **Arquitetura Microkernel**:
   - **Desenvolvimento**: Pode ser mais demorada e cara inicialmente, pois envolve a criação de um núcleo mínimo e a implementação de serviços adicionais como processos separados.
   - **Manutenção**: Mais fácil e menos custosa, já que os componentes são isolados. Atualizações e correções podem ser feitas em módulos específicos sem impactar o núcleo do sistema.

3. **Arquitetura em Camadas**:
   - **Desenvolvimento**: Moderadamente complexa, pois cada camada deve ser bem definida e interagir corretamente com as outras.
   - **Manutenção**: Relativamente fácil, pois problemas podem ser isolados e corrigidos em camadas específicas sem afetar o restante do sistema.

#### Segurança da Informação

1. **Arquitetura Monolítica**:
   - **Segurança**: Pode ser mais vulnerável, pois uma falha em qualquer parte do sistema pode comprometer todo o SO. A integração de todos os componentes em um único bloco de código pode dificultar a implementação de medidas de segurança robustas.

2. **Arquitetura Microkernel**:
   - **Segurança**: Geralmente mais segura, pois isola os serviços em processos separados. Isso limita o impacto de uma falha ou ataque a um único componente, protegendo o núcleo do sistema e outros serviços.

3. **Arquitetura em Camadas**:
   - **Segurança**: Oferece um bom equilíbrio, pois cada camada pode implementar suas próprias medidas de segurança. No entanto, a comunicação entre camadas deve ser cuidadosamente gerenciada para evitar vulnerabilidades.

### Conclusão

A escolha da arquitetura de um sistema operacional tem um impacto significativo tanto no custo de desenvolvimento e manutenção quanto na segurança da informação. Arquiteturas monolíticas podem ser mais rápidas e baratas de desenvolver inicialmente, mas podem acarretar custos de manutenção mais altos e maiores riscos de segurança. Por outro lado, arquiteturas microkernel e em camadas podem exigir um investimento inicial maior, mas oferecem vantagens em termos de manutenção e segurança.

## Questão
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:
- Complexidade de implementação e manutenção
- Necessidade de especialização da equipe
- Potenciais vulnerabilidades de segurança
- Facilidade de atualização e correção de falhas

**Dica:** Utilize exemplos de sistemas operacionais reais que adotam essas arquiteturas para ilustrar sua análise.

**Copilot informa**: Essa questão incentiva os alunos a considerarem tanto os aspectos econômicos quanto os de segurança ao avaliar diferentes arquiteturas de sistemas operacionais.

## Resposta
- Complexidade de implementação e manutenção

Monolítica -> No sistema monolítico e implementado em um bloco maciço, onde o código que está operando tem acesso a todos os recursos do hardware e sem restrições quando se trata de acessar a memória, já a manutenção do sistema monolítico é mais complexa e mais custosa devido os componentes do sistema terem acesso um ao outro de forma irrestrita,ou seja qualquer erro pode afetar várias partes do sistema.

Microkernel -> No microkernel a implementação é feita por meio da separação do código de alto nível e de baixo nível, onde o hardware irá apenas gerenciar o código de baixo nível e outras abstrações básicas, e a manutenção desse sistema e mais fácil e menos custosa devido os componentes serem isolados desse modo os erros podem ser corrigidos de forma individual, não afetando as outras partes do sistema.

Camadas -> No sistema de camadas a implementação é feita por meio da divisão de camadas: camada inferior a qual tem acesso total com o hardware, camada intermediária responsável pela abstração e gerência e a camada superior seria a interface do núcle para as aplicações, a manunteção desse sistema é fácil devido o sistema ser separado em camadas.

- Necessidade de especialização da equipe

Monolítica -> Devido o sistema monolítico ser conectado, sem restrições e qualquer modificação pode afetar várias partes do sistema é necessário se ter uma equipe com uma boa base em desenvolvimento e manuntenção de sistemas. 

Microkernel -> No microkernel é necesário se ter uma equipe bastante especializada devido sua arquitetura ser baseada em sistemas isolados, sendo assim, cada problema pode ser muito diferente do outro, além de que esses sistemas são implementados em contextos altamente especializados como: sistemas embarcados, dispositivos de tempo real entre outros.

Camadas -> O sistema de camadas não requer tanta especialização sendo mais fácil de manipular do que o microkernel, mas exige um certo nível de conhecimento para que as camadas sejam gerenciadas de forma certa sem nenhum erro.

- Potenciais vulnerabilidades de segurança

Monolíticas -> O sistema monolítico é bastante vulnerável pelo fato do sistema ser todo conectado e sem nenhuma restrição, sendo assim, Qualquer brecha no sistema pode ter um impacto significativo, comprometendo a segurança e a integridade de toda a aplicação.

Microkernel -> Devido ao fato do sistema microkernel ser feito em forma de blocos isolados onde cada parte do sistema não depende da outra ele possui é mais seguro e menos vulnerável, mas isso  não quer dizer que ele está imune a ataques.

Camadas -> O sistema de camadas também é mais seguro pois se uma camada foi afetada o restante do sistema não necessariamente vai ser comprometido.

- Facilidade de atualização e correção de falhas

Monolíticas -> A facilidade de atualização e correção de falhas no sistema monolítico pode ser meio limitada devido ao fato dele ser todo conectado ou seja uma atualização/correção de falha será necessário mexer no sistema todo para que isso seja solucionado.

Microkernel -> No microkernel a facilidade de atualização e correção de falhas é mais fácil do que no sistema monolítico porém requer uma atenção maior na parte de coordenação entre os módulos e compatibilidade durante as alterações.

Camadas -> No sistema baseado em camadas as facilidade de atualização e correção são facilitadas devido as camadas oferecerem boa modularidade, porém pode se tornar complexo de acordo com o tamanho do sistema.

# Questão 3. Introdução à Segurança de Sistemas Operacionais

## Texto informativo

A segurança de um sistema operacional é um aspecto crucial que visa proteger os recursos do sistema contra acessos não autorizados, ataques maliciosos e falhas. Um sistema operacional seguro deve garantir a integridade, confidencialidade e disponibilidade dos dados e serviços. Para alcançar esses objetivos, várias técnicas e mecanismos são implementados, incluindo:

1. **Controle de Acesso**: Define quem pode acessar o sistema e quais recursos podem ser utilizados. Isso é feito através de autenticação (verificação de identidade) e autorização (permissão de acesso).

2. **Criptografia**: Utilizada para proteger dados em trânsito e em repouso, garantindo que apenas usuários autorizados possam acessar informações sensíveis.

3. **Auditoria e Monitoramento**: Registra atividades do sistema para detectar e responder a comportamentos suspeitos ou anômalos.

4. **Isolamento de Processos**: Garante que os processos sejam executados em ambientes isolados, evitando que um processo comprometa a segurança de outro.

5. **Atualizações e Patches**: Manter o sistema operacional atualizado é essencial para corrigir vulnerabilidades conhecidas e proteger contra novas ameaças.


## Questão

Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:
- Benefícios e desafios de cada mecanismo
- Impacto na experiência do usuário
- Exemplos de situações onde esses mecanismos são críticos

**Dica:** Pense em como esses mecanismos são aplicados em sistemas operacionais que você utiliza no dia a dia, como Windows, Linux ou macOS.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre o equilíbrio entre segurança, performance e usabilidade, aplicando conceitos teóricos a contextos práticos.

## Resposta
- Benefícios e desafios de cada mecanismo

Controle de acesso -> Para o controle de acesso temos os benefícios como segurança e proteção contra acesso não autorizado, já para os desafios temos complexidade e performance.

Criptografia -> Na criptografia os benefícios são maior segurança principalmente contra roubo de dados e maior confidenciabilidade dos dados, já para os desafios temos perfomance e complexidade

Auditoria e Monitoramento -> para auditoria e monitoramento temos os seguintes benefícios: detecção de ameaças, rastreamento de atividades e confirmade, já para os desafios temos a sobrecarga de perfomance, armazenamento e análise de dados e alertas falsos.

Isolamento de Processos -> para Isolamento de Processos é possível identificar os seguintes benefícios: segurança, estalabilidade e proteção de dados, já para os desafios temos pricipalmente a complexidade de comunicação e gerenciamento de recursos.

Atualizações e Patches -> no controle de Atualizações e Patches temos os principais benefícios sendo correção de vulnerabilidades e melhoria de desempenho, já para os desafios temos compatibilidade e riscos de falhas.

- Impacto na experiência do usuário

Controle de acesso -> O controle de acesso em geral tem impacto positivo na experiência do usuário tendo em vista que a melhora na segurança garante que apenas os usuários desejados vão ter acesso aos arquivos desejados impedindo que pessoas não autorizadas tenham esse acesso.

Criptografia -> A criptografia em maior parte tem um impacto na experiência do usuário pois ela garante maior segurança e confidencialidade nos dados dos usuários.

Auditoria e Monitoramento -> A auditoria e monitoramento podem impactar de forma negativa na experiência do usuário se forem implementadas de forma errada, porém elas são essenciais quando o assunto é garantir mais segurança e confidencialidade ao usuário.

Isolamento de Processos -> O isolamento de processos dependendo da forma que é implementada pode impactar negativamente queda da perfomance devido ao consumo adicional de recursos, mas em geral ela melhora principalmente a segunraça e também a estabilidade do sistema.

Atualizações e Patches -> Atualizações e Patches são essenciais para manter um sistema funcional, porém seu impacto é relativo quando se trata da experiência do usuário podendo impactar tanto negativamente quanto positivamente.

- Exemplos de situações onde esses mecanismos são críticos

Controle de acesso -> O controle de acesso tem um principal papel quando se trata de proteção dados sensíveis, evitando acessos não autorizados, fraudes e vazamentos de dados, sendo trivial para que uma boa segurança seja garantida nos sistemas do dia a dia.

Criptografia -> A criptografia geralmente tem um papel fundamental quando se trata de mensagens, transações financeiras e comunicações em redes públicas atuando principalmente na confidencialidade e garantia de que sua mensagem não sera interceptada por terceiros, gerando assim, uma maior segurança nos seus dados.

Auditoria e Monitoramento -> A Auditoria e Monitoramento são essencias para garantir segurança, integridade e disponibilidade dos sistemas sendo de suma importância para que os mesmos funcionce de forma correta e segura.

Isolamento de Processos -> O isolamento de processos é fundamental quando se trata do funcionamento independente dos aplicativos, impedindo que os mesmos interfiram nas ações uns dos outros o que acaba por resultar em uma melhor estabilidade do sistema.

Atualizações e Patches -> As atualizações e patches são indispensáveis quando o assunto é  estabildiade e perfomance do sistema, atuando principalmente na correção de bugs e falhas que podem ser prejudicias ao sistema.


# Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

## Texto informativo

O escalonamento de processos é uma função crítica de um sistema operacional, responsável por determinar a ordem em que os processos são executados pelo processador. O objetivo é maximizar a eficiência do sistema, garantindo que os recursos sejam utilizados de maneira justa e eficaz. No entanto, encontrar o algoritmo de escalonamento ótimo envolve um equilíbrio delicado entre o custo de processamento e a eficiência do escalonamento.

### Custo de Processamento

O custo de processamento refere-se ao tempo e aos recursos necessários para executar um algoritmo de escalonamento. Algoritmos mais complexos podem oferecer melhores resultados em termos de tempo de resposta e utilização do processador, mas também podem exigir mais recursos computacionais para tomar decisões de escalonamento. Isso pode incluir tempo de CPU, memória e outras operações de sistema.

### Algoritmo Ótimo de Escalonamento

Um algoritmo ótimo de escalonamento é aquele que maximiza a eficiência do sistema operacional, minimizando o tempo de espera dos processos, o tempo de resposta e o tempo de retorno. Alguns dos algoritmos de escalonamento mais comuns incluem:

- **First-Come, First-Served (FCFS)**: Simples e fácil de implementar, mas pode levar a longos tempos de espera para processos curtos.
- **Shortest Job Next (SJN)**: Minimiza o tempo médio de espera, mas pode ser difícil de implementar devido à necessidade de prever o tempo de execução dos processos.
- **Round Robin (RR)**: Oferece uma abordagem justa, atribuindo fatias de tempo iguais a todos os processos, mas pode resultar em maior sobrecarga de contexto.
- **Priority Scheduling**: Processos com maior prioridade são executados primeiro, mas pode levar à inanição de processos de baixa prioridade.

## Questão

Considerando os conceitos de custo de processamento e algoritmo ótimo de escalonamento, analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador. Em sua resposta, aborde os seguintes pontos:
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento
- Impacto do custo de processamento na escolha do algoritmo
- Exemplos de situações onde um algoritmo pode ser preferível a outro

**Dica:** Pense em como esses algoritmos são aplicados em diferentes cenários, como sistemas de tempo real, servidores web e sistemas operacionais de uso geral.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre a complexidade e os trade-offs envolvidos na escolha de um algoritmo de escalonamento, aplicando conceitos teóricos a contextos práticos.

## Resposta
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento

Algoritmo escolhido -> First-Come, First-Served (FCFS)

Vantagens

- Simples e fácil de executar
- requer pouca preparação para a programação de recursos 
- fácil de comunicar o processo para parceiros de transporte

Desvantagens

- Execução lenta
- Sem preempção



Shortest Job Next (SJN) 

Vantagens

- Melhor desempenho para processos pequenos
- Simplicidade

Desvantagens

- inanição de processos com longos tempo de execução
- Sobrecarga de Gerenciamento

- Impacto do custo de processamento na escolha do algoritmo

Algoritmo -> First-Come, First-Served (FCFS): O custo do algoritmo FCFS pode variar bastante, se o sistema for de grande tamanho e complexo ele custa bastante devido ao aumento do tempo de espera, porém em sistemas simples ele pode ser bastante eficaz e possuir baixo custo operacional.



Algoritmo -> Shortest Job Next (SJN): o Custo do algoritmo SJN pode variar de acordo com o tempo médio de espera fatores como starvation e complexidade de implementação aumenta o custo desse algoritmo.

- Exemplos de situações onde um algoritmo pode ser preferível a outro
Em sistemas mais simples e de fácil implementação pode ser preferível utilizar o algoritmo FCFS, já em sistemas com recursos limitados, tarefas não iterativas e com processos muitos curtos é melhor se usar o SJN. 


# Questão 5. Aplicativo em python vs aplicativos em c

## Questão

Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware. Em sua resposta, considere os seguintes pontos:
- O papel do interpretador no caso do Python
- O processo de compilação no caso do C
- A interação entre o kernel do sistema operacional e os drivers de dispositivo
- A tradução final das instruções para o formato binário (0 e 1) executado pelo hardware

**Dica:** Compare e contraste os dois processos, destacando as principais diferenças e semelhanças na forma como as instruções são processadas e executadas.

**Copilot informa**: Essa questão incentiva os alunos a refletirem sobre os diferentes caminhos que as instruções seguem em linguagens interpretadas e compiladas, aplicando conceitos teóricos a contextos práticos.
