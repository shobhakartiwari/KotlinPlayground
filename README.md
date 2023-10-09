# KotlinPlayground
This is used to write code in kotlin 

/**
 * You can edit, run, and share this code.
 * play.kotlinlang.org
 */
fun main() {
    println("Hello, world!!!")
    val result = sumOfTwoNum(1, 3)
    println("sum = $result")
    val a : Int = 1
    val sum = sumOfOptionalNum(a,a)
    println("sum = $sum")
    val array  = arrayOf("1","2","3","4","5","6")
    val evenSum = sumOfEvenfrom(array)
    println("total sum of even = $evenSum")
}


// function to find the sum of two number
fun sumOfTwoNum(n1:Int, n2:Int) : Int {
    val result = n1 + n2
    return result
}

// function to find the sum of two optional numbers
fun sumOfOptionalNum(a: Int?, b: Int?): Int {
    return (a ?: 0) + (b ?: 0)
}

//find the sum of even numbers from an array of string
fun sumOfEvenfrom(stringArray:Array<String>) : Int {
    val intArray = stringArray.map{it.toInt()}
    val evenArray = intArray.filter{it % 2 == 0}
    val sum = evenArray.reduce{acc, element -> acc + element}
    return sum
}
