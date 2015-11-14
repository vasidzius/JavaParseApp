# JavaParseApp
Приложение написано по следующему заданию:
 * 1. Построить AST для приведенного скрипта - это значит разобрать java-код в указанном файле на Абстрактное Синтаксическое Дерево.
      Для этого использую Javaparser - https://github.com/javaparser/javaparser
 * 2. Добавить новый метод `fib` для класса `D`, в задачи которого будет входить рекурсивное вычисление n-го числа ряда Фибоначчи, где `n`-передается в качестве значения единственного аргумента 
      Это значит, что программно нужно изменить полученное AST, добавив метод fib в конкретное место кода
 * 3. Заменить каждое из значений массива переменной `c` метода `baz` на вызов метода `fib`, где аргументом будет достаточное значение числа для получения заменяемого значения массива и возможного остатка;
      Опять же, программно изменить AST
 * 4. Произвести оптимизацию кода метода `foo` класса `D` (удаление мертвого кода);
      Самый сложный момент - *КОРРЕКТНОЕ* удаление необходимым узлов AST
 * 5. Преобразовать результирующий AST обратно в Java-код;
 * 6. Написать юнит-тесты.
 
Например, приложение может оптимизировать такой код:
```java
class D {

public int foo(int e) {
    int a = 20,
        b = a + 15;
      }
}
```
на выходе:
```java
class D {

public int foo(int e) {
    int b = 35;
      }
}
```

Подробное описание читайте начиная с MainClass.java

