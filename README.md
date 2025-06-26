# Exercícios Kotlin Básico

Este repositório contém exercícios básicos em Kotlin para iniciantes, com foco em variáveis, estruturas condicionais, arrays, listas e laços de repetição.  
Os exercícios foram desenvolvidos para fixar conceitos fundamentais da linguagem.

## Exercício 1 — Variável mutável com valor inicial e alteração
Este exercício demonstra o uso de uma variável mutável (`var`) em Kotlin.  
A variável é inicializada com o valor inteiro `6`; em seguida, o valor é alterado para outro número; e por fim, o valor atualizado é impresso no console.

```kotlin
fun main() {
    var numero = 6
    println("Valor inicial: $numero")

    numero =  10

    println("Novo valor: $numero")
```
## Exercício 2 — Variável imutável e tentativa de alteração
Demonstra a criação de uma variável imutável (`val`) e a tentativa de alteração, que não é permitida. Para ilustrar, foi criada uma variável mutável separada.

```kotlin
fun main() {
    val numero1: Int = 6
    println("Valor inicial: $numero1")

    var numero2: Double = 7.0
    val valorAlterado = numero2.toDouble()
    println("Novo valor: $valorAlterado")
}
```

## Exercício 3 — Verificar se um número é par usando (if/else)
Cria uma variável e verifica se ela é par ou não usando o comando `if/else`. Imprime o resultado na tela.

```kotlin
fun main() {
    var numero1 = 10

    if(numero1 % 2 == 0){
        println("O numero e par")
    } else {
        println("O numero nao e par")
    }
}
```

## Exercício 4 — Verificar se um número é par ou ímpar usando (when)
Utiliza a expressão `when` para verificar se um número é par ou ímpar e imprime o resultado.

```kotlin
fun main() {
    var numero = 5
    var parImpar: String

    parImpar = when {
        numero % 2 == 0 -> "par"
        else -> "impar"
    }

    println("O numero $numero e $parImpar")
}
```

## Exercício 5 — Inicializa uma array com 40 posições e preenche com valores de 0 a 39
Cria uma `array` de 40 posições e preenche cada posição com o índice correspondente. Em seguida, imprime os valores.

```kotlin
fun main() {
    val array: IntArray = IntArray(40)

    for (i in array.indices) {
        array[i] = i
        println(array[i])
    }
}
```

## Exercício 6 — Cria uma lista de inteiros contendo números de 1 a 99 usando (for)
Cria uma lista mutável e preenche com os números de 1 até 99 usando um laço `for`. Depois imprime todos os números.

```kotlin
fun main() {
    var lista = mutableListOf<Int>()

    for(i in 1..99) {
        lista.add(i)
    }

    for (i in lista) {
        println(i)
    }
}
```

## Exercício 7 — Somar todos os itens de uma lista usando (while)
Usa uma estrutura `while` para somar todos os itens de uma lista previamente preenchida e imprime o resultado.

```kotlin
fun main() {
    val lista = mutableListOf<Int>()

    for (i in 1..99) {
        lista.add(i)
    }

    var somaTotal = 0
    var i = 0

    while (i < lista.size) {
        somaTotal += lista[i]
        i++
    }

    println("A soma total dos itens da lista e: $somaTotal")
}
```
