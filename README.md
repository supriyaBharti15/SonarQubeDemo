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
