# Construção do algoritmo KNN para classificação e regressão

## O objetivo é entender como funciona o KNN sem usar a biblioteca específica

---

# Classificação

---

## Como funciona o algoritmo KNN para classificação

1. **Treinamento (`fit`)**:  
   O modelo recebe os dados de treino (`X_train` e `y_train`) e os armazena.  
   Não há aprendizado explícito — o KNN é um método baseado em instâncias.

2. **Distância Euclidiana (`_euclidean_distance`)**:  
   Para cada ponto a ser classificado, calculamos a distância Euclidiana para todos os pontos do conjunto de treino.

3. **Previsão (`predict`)**:  
   - Para cada ponto de teste, identificamos os `k` vizinhos mais próximos (menores distâncias).  
   - Extraímos as classes (rótulos) desses vizinhos.  
   - Fazemos uma votação majoritária para decidir a classe do ponto de teste.

---

# Regressão

## Como funciona o algoritmo KNN para regressão

1. **Treinamento (`fit`)**:  
   O modelo armazena os dados de entrada (`X_train`) e seus valores alvo (`y_train`).  
   Diferente de outros modelos, não há ajuste de parâmetros — o aprendizado é "preguiçoso".

2. **Distância Euclidiana (`_euclidean_distance`)**:  
   Para cada ponto de teste, calculamos a distância Euclidiana para todos os pontos de treino.

3. **Previsão (`predict`)**:  
   - Identificamos os `k` vizinhos mais próximos no espaço das features.  
   - Pegamos os valores reais (`y_train`) desses vizinhos.  
   - A previsão é a **média** dos valores dos vizinhos selecionados.
