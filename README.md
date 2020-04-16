# SonarQubeDemo
SonarQube integration with android studio project using local host

# Kotlin
## Mutable and Immutable in Kotlin
```kotlin
# Mutable
   var name: String
   name = "supriya"
   Log.d("::TAG::", name)
   ```
   ```kotlin
# Immutable
 val roll = "123"
 Log.d("::TAG::", "roll=" + roll)
 ```
## String Templates in Kotlin
```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        //Create object in kotlin
        var q = Question()
        
        //now print Question first
        println(q.question)
        println("Answer given by you is:=${q.answer}")
        println("Correct Answer is:=${q.correctAnswer}")
        
        //Change value of variable in class Question
        q.answer = "30"
        println("::TAG:: update Answer is ${q.answer}")
        
        //call method from class  Question
        println("::TAG:: call method from Question ${q.display()}")
    }
```
```kotlin
//this is Question Class
class Question {
        var answer = "22"
        val correctAnswer = "31"
        val question = "How many days in Jan Month?"

        fun display() {
            println("Your Correct Answer is = $correctAnswer")
        }

    }
 ```
 ## if expression 
 //compare two string using ==
 ```kotlin
        val result = if (q.answer == q.correctAnswer) {
            "Answer is correct"
        } else {
            "Answer is incorrect"
        }
        println("::TAG::  $result")
 //Output ::-- System.out: ::TAG::  Answer is correct

```

//compare using .equals() method
```kotlin
        
        val result1 = if (q.answer.equals(q.correctAnswer)) {
            "Answer Right"
        } else {
            "Answer Wrong"
        }
        println("::TAG::  $result1")
  //Output ==== System.out: ::TAG::  Answer Right
 ```
 ## null handling in Kotlin
 ```kotlin
        //create object of Question class
        //if we wants or know that any value can be null then we have to decleare value like below using ? symbol
        val q: Question? = null
        println("::TAG:: ${q?.answer} is ${q?.question}") // mendentory to check null before using object 
        //output== ::TAG:: null is null , because here null assign to object q 
 ```
## when statement in Kotlin
```kotlin

```
```kotlin
//Question Class which method we will access in main class //when statement in Kotlin
        val q = Question()
        println("::TAG::${q.printResult()}")

        //now change value of answer and see the result
        q.answer="31"
        println("::TAG::${q.printResult()}")
class Question {
        var answer = "22"
        val correctAnswer = "31"

        fun printResult() {
            when (answer) {
                correctAnswer -> println("::TAG:: u r right")
                else -> println("::TAG:: u r wrong")
            }
        }
    }
```
