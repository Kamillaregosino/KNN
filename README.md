# Algoritmo de Aprendizado Supervisionado KNN

## É um algoritmo de classificação e regressão baseado em distâncias. Ele é útil especialmente para dados limpos, mas ele não constrói um modelo durante o treino, apenas armazena os dados.

---

# Classificação

1. Fornece um ponto para classificar;
2. O KNN mede a distância entre esse ponto e todos os pontos do conjunto de treino;
3. Seleciona os K vizinhos mais próximos;
4. A classe mais comum entre esses vizinhos define a classe predita (por votação).

---

# Regressão

**Diferente da classificação, ao invés de votar, ele tira a média dos valores dos K vizinhos mais próximos.**

---

# Passos Técnicos

1. Escolher K ( número de vizinhos);
2. Calcular a distancia;
3. Selecionar os K vizinhos mais próximos;
4. Decidir a saída ( voto para classificação ou média para regressão).

---

# Tipos de Distâncias

1. Euclidiana: distância entre 2 pontos;
2. Manhattan: somatória da diferença absoluta das coordenadas;
3. Minkowski: Ela define uma métrica de distância entre dois pontos em um espaço vetorial, controlada por um parâmetro 𝑝.

---

# Dicas

1. **Escolha do K:** Número ímpar para classificação binária e usar validação cruzada para escolher o melhor K;
2. **Normalização:** Usar StandardScaler ou MinMaxScaler para noralização;
3. **Dados ruidosos:** Outliers afetam o desempenho, então deve-se ponderar vizinhos mais próximos;
4. **Desempenho:** Custo alto com dados grandes.

---

# Funcionamento 

1. Calcular a distancia entre o ponto de teste e todos os pontos de treino;
2. Ordenar os pontos pela menor distancia;
3. Pegar os k vizinhos mais próximos;
4. Retornar a classe mais comum entre os vizinhos.

