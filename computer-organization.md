### Computer Organization

## October 9th

**Políticas de memória**: tomadas de decisões do hardware (ex: memória cache ou principal?)

Pipeline - ?

**ISA** - Instruction set architecture

Todo programa em execução roda na memória principal

## October 10th

Acessar a memória principal é muito mais demorado do que acessar o processador, por isso a necessidade do cache - evita bottleneck

**4 Proposições de Von Neumann**<br>
1. Concebeu-se os computadores com estas 4 unidades funcionais:
- Processamento de informações (CPU)
- Memória principal - armazena instruções e dados
- Dispositivos de entrada e saída - teclado, mouse, placa de vídeo, rede, ssd, hd

2. Uso da aritmética binária, ao invés de usar 10 níveis de tensão como os de 1a geração.

3. Ciclo de instrução repetitivo
   
|N|Etapa|Descrição|
|--|--|--|
|1|Busca da instrução|quando o programa entra em execução, carregamos na memória principal. Buscamos a instrução na memória e carregamos no processador através do Program Counter, um registrador que nos informa o local da instrução na memória.|
|2|Decodificar a instrução|olhar o código para definir a operação.|
|3|Buscar os operandos|acessar o banco de registradores para obter os dados necessários.|
|4| Executar a instrução|informar a ULA, através da decodificação, qual operação ela deve fazer com os operandos|
|5|Armazenar o resultado|encontrar o registrador alvo e armazenar o resultado da operação.|

4. Programa armazenado em memória - programa em execução roda na memória principal. Lembrar do cache. 

**Arquitetura de Von Neumann** - A memória é concorrida, com uma só entrada, então só podemos fazer o passo 1 ou o passo 3 um de cada vez.<br>
**Arquitetuta de Harvard** - Ou a memória tem duas entradas, ou temos duas memórias. Memória cache nível 1 - 16x16, duas entradas, uma pra instruções e outra pra dados.

**Barramento local (Front-side bus):** relacionamento memória-CPU.

## October 17th

Todos os tamanhos de processador tem sua demanda.

ARQUITETURA ARTELIS (AMD): Redes intra-chip fazendo a comunicação dos chips por roteadores.

Software service/Platform service/Infrastructure service

ILP - Instruction Level Paralelism está maximizada, então trabalhamos com modelos novos como de dados (DLP), threads (TLP) e de requisições (RLP).

**Arquitetura do conjunto de instruções**
- Estrutura: Código de operação + operandos
- No máximo 3 operandos: 2 de origem e 1 de destino

