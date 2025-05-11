# Sistema de Busca de Candidatos Políticos

## Descrição
Este projeto implementa um sistema em C para gerenciar e buscar informações de candidatos políticos a partir de um arquivo de dados (`candidatos.txt`). Foi desenvolvido para conclusão da disciplina de **Algoritmos e estruturas de dados II**(3° periódo), do curso Ciência da computação - UFU . O sistema suporta três métodos de busca:

1. **Busca Binária**: Utiliza um vetor ordenado para buscar candidatos por estado, cidade ou número.
2. **Árvore Binária**: Organiza os candidatos em uma árvore binária ordenada por estado.
3. **Árvore AVL**: Organiza os candidatos em uma árvore AVL balanceada ordenada por número.

O programa oferece um menu interativo que permite filtrar candidatos por estado, cidade ou número, com opções para exibir detalhes adicionais (gênero, partido, cor/raça).

## Funcionalidades
- **Leitura de Dados**: Carrega informações de candidatos a partir de um arquivo de texto (`candidatos.txt`).
- **Ordenação**: Usa o algoritmo Shell Sort para ordenar candidatos por estado, cidade ou número.
- **Busca por Estado**: Lista todos os candidatos de um estado específico.
- **Busca por Cidade**: Lista candidatos de uma cidade específica dentro de um estado.
- **Busca por Número**: Exibe detalhes completos de um candidato com base em seu número, estado e cidade.
- **Medição de Desempenho**: Calcula o tempo de carregamento e busca para cada método (busca binária, árvore binária, AVL).
- **Interface Interativa**: Menu em console para facilitar a interação com o usuário.

## Limitações e Possíveis Melhorias
- **Busca por Número**: A função `filtrar_por_numero_bb` na busca binária tem uma lógica complexa e pode não funcionar corretamente. Considere simplificá-la ou usar uma busca linear após filtrar por estado e cidade.
- **Recursão**: As funções de busca em árvores usam recursão, que pode causar stack overflow em conjuntos de dados muito grandes. Para grandes volumes, substitua por iteração com uma pilha explícita.
- **Tratamento de Acentos**: O programa não normaliza acentos, o que pode causar falhas em comparações de strings (ex.: `CÓRREGO` vs. `CORREGO`). Use bibliotecas como `iconv` para normalização.
- **Liberação de Memória**: O programa não libera a memória das árvores binária e AVL. Adicione funções para liberar os nós antes de encerrar.
- **Validação de Entrada**: O programa não valida entradas do usuário (ex.: estados inválidos). Adicione verificações para melhorar a robustez.
- **Desempenho**: A árvore binária pode se degenerar em uma lista ligada se os dados forem inseridos em ordem. Embaralhe os dados antes da inserção ou use apenas a AVL.
