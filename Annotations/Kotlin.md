### Getters and Setters
Por padrão no Kotlin, não é necessário fazer a definição explícita dos getters and setters das propriedades, ao definir o atributo, já é definido também seu getter e setter default.

Porém, é possível personalizar, caso queira

```kotlin
val width = 0

val height = 0

// Retornando a área diretamente dos atributos width e height alterando o getter
val area get() = this.width * this.height
	set(value) {  // Demonstrando como cria o setter
		value++
	}
```

### Companion Objects
É a forma de criar constantes estáticas dentro de uma classe no Kotlin

```kotlin
class Mathematics {
	companion object {
		val PI = 3.14
	}
}

Mathematics.PI // this works lol
```

### Object Expressions

É possível também criar expressões de objetos, que seriam como uma classe de uso único, como uma classe lambda

```kotlin
val cabeca = object {
	val olho = "olho"
	val boca = "boca"

	override fun toString() = 
	return "$olho $boca"
}

println(cabeca) // olho boca
```