```
@startuml
!theme mars

title Use Case Diagram

RECTANGLE System {
    (Search for additional information) as Search 
    (Object processing) as ObjProcessing
    (System update) as Update
    (Debugging) as Debug
    (Interactive content upload) as UploadContent 
    (Problem solving) as Solver
    (Formula processing) as Formulas
    (Text processing) as Text
    (Explanations of text information) as Explanation
    (Copying text) as Copying
    (Formula solving) as SolveFormula
    (Explanation of formulas) as ExplFormula
    (Knowledge base update) as DbUpdate
    (Interactive test completion) as PassingTest
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
@enduml

```