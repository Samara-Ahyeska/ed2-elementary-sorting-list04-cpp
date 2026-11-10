# Estrutura de Dados II — Exercícios de Fixação (Merge Sort e Quick Sort)

**Instituição:** Instituto Federal de Educação, Ciência e Tecnologia do Triângulo Mineiro (IFTM) - Campus Patrocínio  
**Curso:** Tecnologia em Análise e Desenvolvimento de Sistemas (4º Período)  
**Disciplina:** Estrutura de Dados II  
**Professor:** Júnio Moreira  

## 📑 Sumário

- [Visão Geral](#-visão-geral)
- [Estrutura do Repositório](#-estrutura-do-repositório)
- [Questões](#-questões)
  - [Questão 1: Contagem de Inversões com Merge Sort](#questão-1-contagem-de-inversões-com-merge-sort)
  - [Questão 2: O Desafio da Estabilidade: Merge Sort vs. Quick Sort](#questão-2-o-desafio-da-estabilidade-merge-sort-vs-quick-sort)
  - [Questão 3: Seleção Linear com Particionamento de Lomuto (Quickselect)](#questão-3-seleção-linear-com-particionamento-de-lomuto-quickselect)
  - [Questão 4: Ordenação Par-Ímpar com Particionamento de Hoare](#questão-4-ordenação-par-ímpar-com-particionamento-de-hoare)

---

## 🔍 Visão Geral

Este repositório contém os exercícios de fixação da disciplina de **Estrutura de Dados II**. Os problemas abordam tópicos fundamentais do paradigma de Divisão e Conquista (Merge Sort e Quick Sort), análise de complexidade, manutenção de estabilidade, algoritmo de seleção linear (Quickselect) e esquemas de particionamento unidirecional e bidirecional (Lomuto vs. Hoare).

---

## 📁 Estrutura do Repositório

```text
.
├── src/
│   ├── Exer01_MergeSortCountInversions.cpp    # Resolução da Questão 1
│   ├── Exer02_StabilityMergeSortVsQuickSort.cpp # Resolução da Questão 2
│   ├── Exer03_QuickselectLomutoKthLargest.cpp # Resolução da Questão 3
│   └── Exer04_HoarePartitionParitySort.cpp    # Resolução da Questão 4
├── CMakeLists.txt
├── main.cpp
└── README.md                                  # Documentação da lista
```

---

## 📌 Questões

### Questão 1: Contagem de Inversões com Merge Sort

- **Objetivo:** Ordenar um vetor de $N$ inteiros distintos em ordem crescente e determinar a quantidade exata de inversões (pares de índices $(i, j)$ tais que $i < j$ e $A[i] > A[j]$).
- **Abordagem:** Adaptação da etapa de intercalação (*merge*) do Merge Sort para incrementar de forma cumulativa as inversões em complexidade $\mathcal{O}(N \log N)$, evitando a contagem quadrática do Bubble Sort.
- **Entrada/Saída:** Recebe $N$ inteiros distintos; imprime o vetor ordenado na primeira linha e o total de inversões na segunda linha.

### Questão 2: O Desafio da Estabilidade: Merge Sort vs. Quick Sort

- **Objetivo:** Investigar o contraste de estabilidade entre o Merge Sort e o Quick Sort ao ordenar palavras pelo comprimento em ordem decrescente, preservando a ordem original de palavras com tamanhos iguais.
- **Abordagem:** 
  - **Merge Sort (Estável):** Condição de desempate na intercalação prioriza elementos da partição esquerda.
  - **Quick Sort (Instável):** Trocas de longa distância no particionamento alteram a ordem relativa original.
- **Entrada/Saída:** Recebe $N$ palavras; exibe os resultados precedidos pelas marcas `[MergeSort]` e `[QuickSort]`.

### Questão 3: Seleção Linear com Particionamento de Lomuto (Quickselect)

- **Objetivo:** Encontrar o $K$-ésimo maior elemento de uma sequência em tempo linear médio $\mathcal{O}(N)$ utilizando o algoritmo Quickselect com particionamento de Lomuto.
- **Abordagem:** Descarte recursivo da metade irrelevante a cada partição e contagem estrita de trocas efetivas entre posições distintas da memória ($i \ne j$).
- **Entrada/Saída:** Recebe $N$, $K$ e a sequência de inteiros; imprime o valor buscado, o estado final do vetor em memória e a quantidade total de trocas efetivas.

### Questão 4: Ordenação Par-Ímpar com Particionamento de Hoare

- **Objetivo:** Reorganizar um vetor de inteiros positivos em tempo $\mathcal{O}(N)$ e memória auxiliar $\mathcal{O}(1)$, de forma que todos os números pares antecedam os ímpares.
- **Abordagem:** Utilização do particionamento com ponteiros convergentes de Hoare para segregação por paridade, seguida da ordenação crescente da partição par e decrescente da partição ímpar.
- **Entrada/Saída:** Recebe $N$ inteiros positivos; imprime a sequência resultante contendo pares (crescente) seguidos de ímpares (decrescente).

