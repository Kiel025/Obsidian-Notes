## Notação Big O

Big O é uma notação usada para saber o quão eficiente é um algoritmo, em termos de espaço e de tempo.

Em notação `Big O` não é medido tempo de execução, é medido a forma de mostrar como o algoritmo cresce, seja logaritmicamente, exponencialmente, etc.  

```kotlin
fun printFirst(items: List<string>) {
	println(items[0]) // Big O(1)

	for (item in items) { // Big O(n)
		println(item) // Big O(1)
	}

	for (item in items.size - 1 downTo 0) { // Big O(n)
		println(item)
	}
}

fun main() {
	printFirst(listOf("Kiel", "Santos"))
}
```

A Big O Notation vai sempre pegar a maior notação registrada, no exemplo acima, o algoritmo é Big O(n).

Pelo fato de ser 2 for's no exemplo acima, seria 2 notações Big O(n), porém, na notação Big O, é descartado constantes já que o valor a ser alterado é somente o dentro da notação

Árvore Binária é uma estrutura de dados onde ela tem filhos e nós raízes, cada filho pode ter no máximo dois filhos, seguindo a estrutura de árvore mesmo.

![[Pasted image 20240326103644.png]]

## Pesquisa Binária
Imagine que você é dono de uma empresa e deseja fazer uma ação para um cliente específico, você vai abrir o sistema que utiliza e vai procurar pelo nome do cliente, mas daí percebe que existem milhares clientes cadastrados, como você vai procurar? Digitando o nome, correto? 

Agora imagine que você é o desenvolvedor desse sistema e vai implementar esse algoritmo de busca, qual você utilizaria? O mais recomendado nesse caso é o algoritmo de **Pesquisa Binária**

A Pesquisa Binária consiste em pegar uma lista **ORDENADA** e dividir ela pelo meio, fazer a verificação se é esse número, caso não seja ela verifica se o *target*  é maior ou menor e faz a verificação novamente excluindo os valores que não se encaixam. Isso otimiza MUITO o seu problema, já que algo que antes era Big O(n) agora é Big O(log n), o que reduz drasticamente a quantidade de vezes que o software faz a verificação.

Em Kotlin, temos um exemplo de como é uma pesquisa binária aplicada:

```kotlin
fun main() {

    var list = (1..100).toList()
    var target = 82
	var index = binarySearch(list, target);
    
    if (index != -1) {
        println("O target foi encontrado no index $index")
    } else {
        println("O target ($target) não está na lista")
    }
    
}

fun binarySearch(list: List<Int>, target: Int) : Int {
	var low = 0
	var high: Int = list.size -1
	var mid: Int
	
	while (low < high) {
		mid = (high + low) / 2
		
		if (mid == target) return mid
		
		if (mid > target) high = mid
		
		if (mid < target) low = mid
	}
    return -1
}
```

## Ordenação por Seleção

