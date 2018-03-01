# notes

Just some notes aboute code


Oberon (Revision 1.10.2013 / 3.5.2016)

statement = [assignment | ProcedureCall | IfStatement | CaseStatement |
WhileStatement | RepeatStatement | ForStatement]

Statement sequences:
 If statements
 Case statements
 While statements
 Repeat Statements
 For statements

FOR exsamples:
    FOR v := beg TO end BY inc DO S END

RepeatStatement = REPEAT StatementSequence UNTIL expression

WHILE examples:
    v := beg;
    WHILE v <= end DO S; v := v + inc END

    WHILE j > 0 DO
        j := j DIV 2; i := i+1
    END

    WHILE (t # NIL) & (t.key # i) DO
        t := t.left
    END
    
    WHILE m > n DO m := m – n ELSIF n > m DO n := n – m END

CASE example:
    CASE p OF
        P0: p.b := 10 |
        P1: p.b := 2.5 |
        P2: p.b := {0, 2}
    END

IF Example:
    IF (ch >= "A") & (ch <= "Z") THEN ReadIdentifier
    ELSIF (ch >= "0") & (ch <= "9") THEN ReadNumber
    ELSIF ch = 22X THEN ReadString
    END

Golang code:

https://tour.golang.org/flowcontrol/1

<code>
package main

import "fmt"

func main() {
	sum := 0
	for i := 0; i < 10; i++ {
		sum = sum + i
	}
	fmt.Println(sum)
}
</code>

Go has only one looping construct, the for loop.

The basic for loop has three components separated by semicolons:

    the init statement: executed before the first iteration
    the condition expression: evaluated before every iteration
    the post statement: executed at the end of every iteration

The init statement will often be a short variable declaration, and the variables declared there are visible only in the scope of the for statement.

The loop will stop iterating once the boolean condition evaluates to false.

Note: Unlike other languages like C, Java, or JavaScript there are no parentheses surrounding the three components of the for statement and the braces { } are always required. 


Идти только одна циклы, цикл.

Базовый цикл включает три компонента, разделенных точкой с запятой:

заявление инициализации: выполняется перед первой итерацией
выражение условия: вычисляется перед каждой итерацией
оператор post: выполняется в конце каждой итерации

Оператор init часто будет кратким объявлением переменной, а объявленные там переменные будут видны только в области действия оператора for.

Цикл перестанет повторяться, как только логическое условие примет значение false.

Примечание: в отличие от других языков, таких как C, Java или JavaScript, нет скобок, окружающих три компонента оператора for, и скобки { } всегда требуются.
