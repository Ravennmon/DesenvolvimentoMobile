### Declaração de constantes e variáveis

Kotlin playground //compilador online
- val NAME: DATA TYPE = INITIAL VALUE //declaração de data type em val e var é FACULTATIVA
  - Ex.: cal count: Int = 2 //Data type com primeira letra maiúscula

fun main() {
    val count: Int = 2
    println("Você tem $count mensagens não lidas")
    //retorno: Você tem 2 mensagens não lidas
}

fun main() {
    val unreadCount: Int = 5
    val readCount: Int = 100
    println("Você tem ${unreadCount+readCount} mensagens totais.") //Para realizar uma operação basta usar ${operaçãoAquiDentro}
    //retorno: Você tem 105 mensagens totais.
}

fun main() {
    val unreadCount: Int = 5
    val readCount: Int = 100
    
    val result: Int = unreadCount + readCount
    
    println("Você tem $result mensagens totais.")
    //retorno: Você tem 105 mensagens totais.
}

fun main() {
    val cartTotal = 0
    cartTotal = 20 //val NÃO pode ser ser redeclarado
    println("Total: $cartTotal")
}

fun main() {
    var cartTotal = 0
    cartTotal = 20 //var PODE ser redeclarado
    println("Total: $cartTotal")
}

----- 
fun main() {
    val num1: Int = 1
    val num2: Int = 2
    
    sum(num1, num2) //chamada de uma função passando dois parâmetros
}

fun sum (a: Int, b: Int) { //criação de uma função com dois parâmetros
    println("${a+b}")
}

-----
fun main() {
    val num1: Int = 1
    val num2: Int = 2
    
    val result: Int = sum(num1, num2) //atribui o retorno da função para a val result
    println(result)
}

fun sum (a: Int, b: Int): Int { //Define o tipo de retorno da função
    return a + b
}

-----
fun main() {
    val num1: Int = 1
    val num2: Int = 2
    
    print("Greeting 1: ")
    val message: String = greeting()
    println(message)
   
}

fun greeting(): String {
    return "Hello, World!"
} 

--
fun main() {
    val num1: Int = 1
    val num2: Int = 2
    
    print("Greeting 1: ")
    println(greeting())
   
}

fun greeting(): String {
    return "Hello, World!"
}

-----
#### kotlin switch_case (when(){})

fun main() {
    val month: Int = 10
    
    when(month) {
        1 -> println("January")
        2 -> println("February")
        3 -> println("March")
        4 -> println("May")
        5 -> println("June")
        6 -> println("July")
        7 -> println("June")
        8 -> println("August")
        9 -> println("September")
        10 -> println("October")
        11 -> println("November")
        12 -> println("December")
    }
   
}

fun main() {
    val score: Int = 7
    when(score) {
        in 0.. 6 -> println("Fail")
        in 7.. 10 -> println("Success")
    }
   
}
-----
### kotlin for

fun main() {
    val collection = 1..9 
    for(item in collection) {
        println(item)
    }
    
   
}
-----
### kotlin while

fun main() {
    val collection = 9 
    var i = 0
    
    while(i <= collection) {
        println(i)
        i++
    }
    
   
}
-----
### kotlin if

if (condition) {
//procedure if condition = true
} else {
//procedure if condition = false
}

-----
### Kotlin evolution (from Java-like to Kotlin-Like)

#### Part 1:
fun main() {
   print(updateWeather(21))
}

fun updateWeather(degrees: Int) {
    val description:String
    val color:String
    if(degrees < 10) {
        description="Cold"
        color = "blue"
    }else if (degrees < 25) {
        description="Warm"
        color="Orange"0
    } else {
        description="Hot"
        color="Red"
    }
    
    println("The weather is $description|$color")
}

#### Part 2
fun main() {
   print(updateWeather(5))
}

fun updateWeather(degrees: Int) {
    val (description:String, color:String)=
    if(degrees < 10) {
        Pair("Cold","Blue")
    }else if (degrees < 25) {
        Pair("Warm","Orange")
    } else {
        Pair("Hot","Red")
    }
    
    println("The weather is $description|$color")
}

#### Part 3
fun main() {
   print(updateWeather(5))
}

fun updateWeather(degrees: Int) {
    val (description, color)= when {
        degrees < 10 -> Pair("Cold", "Blue")
        degrees < 25 -> Pair("Warm", "Orange")
        else -> Pair("Hot", "Red")
    }
    
    println("The weather is $description|$color")
}

#### Part 4
fun main() {
   print(updateWeather(5))
}

fun updateWeather(degrees: Int) {
    val (description, color)= when {
        degrees < 10 -> "Cold" to "Blue"
        degrees < 25 -> "Warm" to "Orange"
        else -> "Hot" to "Red"
    }
    
    println("The weather is $description|$color")
}

-----
fun main() {
   val names = listOf("Ana", "Bruno", "Carlos", "Bia") //para manipular essa lista precisa declarar como mutableListOf
   printNames(names)
}

fun printNames(names: List<String>) {
    for(name in names) {
        println(name)
    }
}

-----
