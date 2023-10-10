### Computer Organization

## October 9th

**Políticas de memória**: tomadas de decisões do hardware (ex: memória cache ou principal?)

Pipeline - ?

**ISA** - Instruction set architecture

Todo programa em execução roda na memória principal

## October 10th

Acessar a memória principal é muito mais demorado do que acessar o processador, por isso a necessidade do cache - evita bottleneck

**4 Proposições de Von Neumann**<br>
Concebeu-se os computadores com estas 4 unidades funcionais:
- Processamento de informações (CPU)
- Memória principal - armazena instruções e dados
- Dispositivos de entrada e saída - teclado, mouse, placa de vídeo, rede, ssd, hd

Uso da aritmética binária, ao invés de usar 10 níveis de tensão como os de 1a geração.

Ciclo de instrução repetitivo
|N|Etapa|Descrição|
|--|--|--|
|1|Busca da instrução|quando o programa entra em execução, carregamos na memória principal. Buscamos a instrução na memória e carregamos no processador através do Program Counter, um registrador que nos informa o local da instrução na memória.|
|2|Decodificar a instrução|olhar o código para definir a operação.|
|3|Buscar os operandos|acessar o banco de registradores para obter os dados necessários.|
|4| Executar a instrução|informar a ULA, através da decodificação, qual operação ela deve fazer com os operandos|
|5|Armazenar o resultado|encontrar o registrador alvo e armazenar o resultado da operação.|

Programa armazenado em memória - programa em execução roda na memória principal. Lembrar do cache. 

**Arquitetura de Von Neumann** - A memória é concorrida, com uma só entrada, então só podemos fazer o passo 1 ou o passo 3.

**Arquitetuta de Harvard&& - Ou a memória tem duas entradas, ou temos duas memórias.<br>
Memória cache nível 1 - 16x16, duas entradas, uma pra instruções e outra pra dados.

**Barramento local (Front-side bus):** relacionamento memória-CPU.