# Problema: Autocorreção Inteligente

Imagine que você está desenvolvendo um sistema de correção automática para um teclado inteligente. Sua tarefa é implementar um autocorretor que sugere a palavra correta com base na similaridade com palavras existentes em um dicionário.

Dado um dicionário de palavras válidas e uma palavra digitada pelo usuário, sua função deve retornar:

1. A palavra correta se ela já existe no dicionário.
2. A palavra mais próxima (se houver uma com distância de <= 2).
3. NULL se nenhuma palavra próxima for encontrada.

Distância de edição é o número mínimo de operações necessárias para transformar uma string em outra.
As operações permitidas são:
- Inserção de um caractere.
- Remoção de um caractere.
- Substituição de um caractere.


# Exemplo de Entrada e Saída:

**Entrada:**

List<String> dicionario = List.of("casa", "cama", "carro", "gato", "pato");
String palavra = "caso";

**Saída Esperada:**

"casa" // "caso" está a uma edição de "casa" (substituir "o" por "a").

# Requisitos para a Solução:

1. Implementar uma função corrigirPalavra(List<String> dicionario, String palavraDigitada).
2. Utilizar o algoritmo de distância de Levenshtein para calcular a similaridade entre palavras.
3. Retomar a palavra mais próxima apenas se a distância for <= 2.
4. O código deve ser eficiente, evitando verificações desnecessárias.