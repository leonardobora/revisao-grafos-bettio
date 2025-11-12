# RESUMO RÁPIDO: PROVA DE GRAFOS

## Definições Fundamentais

### Grafo
Estrutura G(V,E) onde:
- **V** = conjunto de vértices (ou nós)
- **E** = conjunto de arestas

### Ordem
Quantidade de vértices do grafo.
- Notação: |V|

### Adjacência
- **Arestas adjacentes**: Duas arestas incidem no mesmo vértice
- **Vértices adjacentes**: Dois vértices ligados por uma aresta são adjacentes

### Grau de Vértice
Número de arestas incidentes no vértice.
- **IMPORTANTE**: Laço conta como grau 2!

### Grau de Entrada/Saída
Aplicável apenas a **grafos orientados** (dirigidos):
- **Grau de Entrada (indegree)**: número de arestas que ENTRAM em um nó
- **Grau de Saída (outdegree)**: número de arestas que SAEM de um nó

### Tipos de Vértices Especiais
- **Vértice Isolado**: Grau = 0 (não tem arestas conectadas)
- **Vértice Pendente**: Grau = 1 (apenas uma aresta conectada)

---

## Tipos de Arestas, Vértices e Grafos

### Tipos de Arestas
- **Laço**: Aresta que inicia e termina no mesmo vértice
- **Arestas Paralelas**: Duas (ou mais) arestas que unem o mesmo par de vértices
- **Ponte**: Aresta cuja remoção torna o grafo desconexo

### Classificação de Grafos

#### Grafo Simples
Grafo sem laços nem arestas paralelas.

#### Multigrafo
Grafo que possui laços e/ou arestas paralelas.

#### Grafo Completo
Todo vértice é adjacente a todos os outros vértices.
- **Notação**: Kn (onde n é o número de vértices)
- **Fórmula de arestas**: n(n-1)/2

#### Subgrafo
Subconjunto de vértices e arestas de um grafo original.

#### Grafo Complementar
Grafo com os mesmos vértices do original, mas com arestas invertidas:
- Se há aresta no original, não há no complementar
- Se não há aresta no original, há no complementar

#### Grafo Bipartido
Vértices podem ser divididos em dois conjuntos U e V, onde:
- Toda aresta conecta um vértice de U a um vértice de V
- Nunca conecta dois vértices do mesmo conjunto

#### Grafo Rotulado vs Valorado
- **Rotulado**: Cada vértice tem um rótulo/nome
- **Valorado (ou ponderado)**: As arestas possuem pesos numéricos

---

## Conceitos de Caminho, Ciclo e Árvores

### Caminho
Sequência de arestas conectando vértices.

### Ciclo
Caminho fechado (começa e termina no mesmo vértice).

### Árvore
Grafo que possui simultaneamente:
1. Conexo (existe caminho entre qualquer par de vértices)
2. Sem ciclos (acíclico)
3. n vértices → n-1 arestas

**Propriedade importante**: Toda aresta de uma árvore é uma ponte!

---

## Euleriano vs Hamiltoniano

### 💡 MACETE PRINCIPAL
- **Euleriano** ≈ Vogais (A/E) = **ARESTA**
- **Hamiltoniano** ≈ Consoantes (H/V) = **VÉRTICE**

### Caminho Euleriano
Percorre **todas as ARESTAS** exatamente uma vez.

**Condição**: Grafo tem 0 ou 2 vértices de grau ímpar.

### Ciclo Euleriano
Caminho Euleriano que começa e termina no mesmo vértice.

**Condição**: Todos os vértices têm grau PAR.

### Caminho Hamiltoniano
Passa por **todos os VÉRTICES** exatamente uma vez.

### Ciclo Hamiltoniano
Caminho Hamiltoniano que forma um ciclo fechado.

---

## Representações de Grafos

### Lista de Adjacência
Cada vértice mantém uma lista de seus vizinhos (vértices adjacentes).

**Exemplo**:
```
A: [B, C]
B: [A, D]
C: [A, D]
D: [B, C, E]
E: [D]
```

### Matriz de Adjacência
Matriz n×n onde:
- Posição [i][j] = 1 se existe aresta entre vértice i e j
- Posição [i][j] = 0 se não existe aresta

**Para grafos não-orientados**: Matriz é simétrica

### Matriz Ponderada (Valorada)
Similar à matriz de adjacência, mas:
- [i][j] = peso da aresta (em vez de apenas 1)
- [i][j] = 0 ou ∞ se não existe aresta

### Matriz de Incidência
Matriz n×m onde:
- **Linhas**: vértices
- **Colunas**: arestas
- [v][e] = incidência do vértice v na aresta e (0, 1 ou 2)

---

## Isomorfismo

### Grafos Isomorfos
Dois grafos G₁(V₁,E₁) e G₂(V₂,E₂) são isomorfos se:
- |V₁| = |V₂| (mesma quantidade de vértices)
- |E₁| = |E₂| (mesma quantidade de arestas)
- Existe uma função bijetora f: V₁ → V₂ que preserva adjacências
- Mesma estrutura (adjacências) mesmo com nomes diferentes

**Como verificar**:
1. Verificar se têm mesmo número de vértices e arestas
2. Verificar se a sequência de graus é igual
3. Tentar encontrar mapeamento que preserve adjacências

---

## Macetes e Dicas de Prova

### Macete 1: Euleriano vs Hamiltoniano
- **Euleriano** ≈ Vogais (A/E) = **ARESTA**
- **Hamiltoniano** ≈ Consoantes (H/V) = **VÉRTICE**

### Macete 2: Grafo Completo
Para grafo completo Kn:
- **Número de arestas** = n(n-1)/2

### Macete 3: Árvore
Um grafo é árvore se satisfaz qualquer 2 das 3 propriedades:
1. É conexo
2. É acíclico (sem ciclos)
3. Tem n-1 arestas (onde n = número de vértices)

### Dica Geral
- **Sempre desenhe um exemplo!** Visualizar ajuda muito.
- Revise imagens e diagramas do resumo antes da prova
- Para problemas de caminho/ciclo Euleriano, conte os graus!
- Para grafos bipartidos, tente colorir com 2 cores

---

## BOA PROVA! 📚✨
