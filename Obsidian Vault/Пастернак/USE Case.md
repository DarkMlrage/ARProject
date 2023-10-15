```
@startuml

skin rose

title Use Case Діаграма

RECTANGLE Система {
    (Пошук дод. інформації) as Search 
    (Обробка об`єктів) as ObjProcessing
    (Оновлення системи) as Update
    (Виправлення помилок) as Debug
    (Завантаження інтерактиву) as UploadContent 
    (Розв`язок задач) as Solver
    (Обробка формул) as Formulas
    (Обробка тексту) as Text
    (Пояснення текст. інформації) as Explanation
    (Копіювання тексту) as  Copying
    (Рішення формул) as SolveFormula
    (Пояснення до формул) as ExplFormula
    (Оновлення бази знань) as DbUpdate
    (Проходження інтеркт. задач) as PassingTest
}

:Developer:
:Teacher: 
:Student:

Teacher --> UploadContent
Student -> Solver
Student -> PassingTest
Teacher -left-> Search
Student --> Search
Developer --> Update
Update ...> Debug : include
Update ...> DbUpdate : include
Solver ---> Formulas
Solver ---> Text
Text ...> Explanation : include
Text ...> Copying : include
Formulas ...> SolveFormula : include
Formulas ...> ExplFormula : include
Search <.down. ObjProcessing : extend 
UploadContent .down..> PassingTest : include
```