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
