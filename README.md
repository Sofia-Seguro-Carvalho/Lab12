# Algoritmos e Tipos Abstratos de Dados

## Lab 12 - Implementações de ADT Stack e ADT Queue com Linked List

Este repositório foi criado a partir de:

- <https://github.com/estsetubal-atad/CProgram_Template> 

Consulte o README se tiver dúvidas sobre a sua utilização.

----

**Objetivos**:

- Utilização da estrutura de dados **linked list** para implementação do *ADT Stack* e *ADT Queue*.
- Sensibilização e comparação de complexidades algorítmicas obtidas com implementações baseadas em *array list* e *linked list*.

**Referências**:

- Aula TP \[13\].
- “Tipos Abstratos de Dados – Linguagem C. Bruno Silva”, disponível no Moodle.
    - :bulb: Ver diagramas/descrição de algoritmos da estrutura de dados *linked list*, capítulo 3.

---

### Organização do projeto VS Code

Os ficheiros relativos ao *ADT Stack* e *ADT Queue* encontram-se nas pastas `stack` e `queue`, respetivamente. As respetivas implementações baseadas em *array list* já estão presentes e completas.

O programa associado ao teste de cada implementação permite verificar se a política de acesso respetiva está a ser respeitada e em seguida faz um teste de *stress* com a inserção e remoção de `100.000` elementos. Isto irá permitir verificar o tempo de execução necessário e estará intimamente relacionado com a complexidade algorítmica das operações implementadas.  

Existe um único *makefile* (veja o seu conteúdo) que compila o programa necessário com a estrutura de dados escolhida, e.g.:

```console
$> make stack
# ou
$> make stack_array
# para executar o programa compilado, usamos sempre:
$> ./prog
```

### 1 | ADT Stack - Implementação

A implementação em `stackLinkedList.c` está parcialmente completa, mas falta a implementação das operações `push`, `pop` e `peek` e `print` que dependerão da abordagem escolhida para a obtenção da política de acesso LIFO. Em traços gerais, a inserção/remoção de elementos terá de ser feita na mesma "extremidade" da estrutura de dados.

1. Forneça a restante implementação das funções `push`, `pop` e `peek` e `print`, considerando o topo da pilha no "início" da estrutura de dados, i.e., no nó `stack->header->next`.

2. Compile e execute o programa, verificando se a política de acesso LIFO está a ser respeitada e o tempo de execução do teste de stress (espera-se uma execução rápida).


### 2 | ADT Stack - Comparação de complexidades algorítmicas

Como se compara esta implementação com a mais eficiente baseada em *array list*, elaborada no laboratório anterior?

3. Preencha a seguinte tabela, analisando as respetivas implementações de cada estrutura de dados e tempos de execução do teste de stress?

Operação     | Array List | Linked List
-------------|------------|------------
`create`     | &nbsp;     | &nbsp;
`destroy`    | &nbsp;     | &nbsp;
`size`       | &nbsp;     | &nbsp;
`isEmpty`    | &nbsp;     | &nbsp;
`clear`      | &nbsp;     | &nbsp;
`push`       | &nbsp;     | &nbsp;
`pop`        | &nbsp;     | &nbsp;
`peek`       | &nbsp;     | &nbsp;
`print`      | &nbsp;     | &nbsp;
Tempo exec.? | &nbsp;     | &nbsp;

4. Por qual optaria utilizar num ambiente real? Justifique.

### 3 | ADT Queue - Implementação das operações "genéricas"

A implementação em `queueLinkedList.c` está praticamente vazia. Mas note que, se vamos utilizar a mesma estrutura de dados, e.g., *linked list*, então a definição desta estrutura de dados, assim como as operações "gerais", e.g., `create`, `destroy`, `size`, `isEmpty` e `clear` são idênticas. 

5. Resolva a *forward declaration* ao definir o conteúdo da `struct queueImpl`.

6. Implemente as operações `create`, `destroy`, `size`, `isEmpty` e `clear`.

### 4 | ADT Queue - Implementação das operações "específicas"

Teremos de obter uma política de acesso FIFO com a manipulação da estrutura de dados *linked list*. Em traços gerais, a inserção/remoção de elementos terá de ser feita em "extremidades" opostas da estrutura de dados.

7. Implemente as operações `enqueue`, `dequeue`, `front` e `print`.

8. Compile e execute o programa, verificando se a política de acesso FIFO está a ser respeitada e o tempo de execução do teste de stress.

9. Preencha a seguinte tabela, analisando as respetivas implementações de cada estrutura de dados e tempos de execução do teste de stress?

Operação     | Array List | Linked List
-------------|------------|------------
`create`     | &nbsp;     | &nbsp;
`destroy`    | &nbsp;     | &nbsp;
`size`       | &nbsp;     | &nbsp;
`isEmpty`    | &nbsp;     | &nbsp;
`clear`      | &nbsp;     | &nbsp;
`enqueue`    | &nbsp;     | &nbsp;
`dequeue`    | &nbsp;     | &nbsp;
`front`      | &nbsp;     | &nbsp;
`print`      | &nbsp;     | &nbsp;
Tempo exec.? | &nbsp;     | &nbsp;

10. Por qual optaria utilizar num ambiente real? Justifique.

### 5 | Verificação de correta gestão de memória dinâmica

11. Verifique a correta gestão de memória dinâmica em ambas as suas implementações (ADT Stack e ADT Qeueue), utilizando para esse efeito o *valgrind*.

---

<bruno.silva@estsetubal.ips.pt>