```
@startuml
actor Teacher as "Teacher" 
actor Student as "Student" 
actor Developer as "Developer" 
database Database as "Database" 

participant "System" as System 
participant "Search" as Search
participant "ObjProcessing" as ObjProcessing 
participant "Update" as Update 
participant "Debug" as Debug 
participant "UploadContent" as UploadContent 
participant "Solver" as Solver 
participant "PassingTest" as PassingTest 
participant "Formulas" as Formulas 
participant "Text" as Text 
participant "Explanation" as Explanation 
participant "Copying" as Copying 
participant "SolveFormula" as SolveFormula 
participant "ExplFormula" as ExplFormula 

Teacher --> UploadContent : "Upload content"
Student -> Solver : "Solve problem"
Student -> PassingTest : "Complete test"
Teacher --> Search : "Search for information"
Student --> Search : "Search for information"
Developer --> Update : "System update"
Update --> Debug : "Debugging"
Update --> Database : "Knowledge base update"
Solver <-- Formulas : "Formula processing"
Solver <-- Text : "Text processing"
Text --> Explanation : "Explanations of text information"
Formulas --> SolveFormula : "Formula solving"
Formulas --> ExplFormula : "Explanation of formulas"
Search <-- ObjProcessing : "Object processing"
UploadContent --> PassingTest : "Interactive test completion"

Activate System
Search --> System : "Initiate search"
System --> Database : "Query database"
Database --> System : "Return search results"
System --> Search : "Return search results"
Search --> ObjProcessing : "Process object"
ObjProcessing --> System : "Return processed object"
System --> Update : "Check for updates"
Update --> System : "Perform update"
System --> Debug : "Debug system"
Debug --> Update : "Return debug information"
System --> UploadContent : "Initiate content upload"
UploadContent --> System : "Upload content"
System --> PassingTest : "Initiate test completion"
PassingTest --> System : "Complete test"
System --> Solver : "Initiate problem solving"
Solver --> System : "Solve problem"
System --> Formulas : "Initiate formula processing"
Formulas --> System : "Process formulas"
System --> Text : "Initiate text processing"
Text --> System : "Process text"
Text --> Explanation : "Provide explanations"
Text --> Copying : "Copy text"
Formulas --> SolveFormula : "Solve formula"
Formulas --> ExplFormula : "Explain formula"
System --> Database : "Initiate knowledge base update"
Database --> System : "Update knowledge base"
System --> PassingTest : "Initiate interactive test completion"
PassingTest --> System : "Complete interactive test"
Deactivate System
@enduml

```

