```
@startuml

skin rose

title Class Diagram


    class Materials {
      +material_ID: int
      +name: string
      +formulas: string
      +description: string
    }

    class User {
        +username: string
        +password: string
        +email: string
        +type: string
        +register()
        +login()
    }

    class ObjectRecognition {
        +object: List
        +recognizeObject()
    }

    class ObjectProcessing {
        +object: List
        +processObject()
        +processObjectWithAREGCommands()
    }


    class VirtualObjectsInteraction {
        +object: List
        +interactWithVirtualObjects()
    }

    class EducationalMaterialsUsage {
        +materials: Materials
        +accessMaterials()
        +takeTests()
    }

    class EducationalOrganizationConnection {
        +username: string
        +typeOfUser: string
        +connectToOrganization()
    }

    class InstitutionMaterialsProvision {
        +username: string
        +materials: Materials
        +provideUniqueMaterials()
        +linkToInstitutionChats()
    }

    class ListManagement {
        +username: string
        +addFriend()
        +removeFriend()
    }

    class ChatUsage {
        +username: string
        +joinChatByLogin()
        +joinPrivateChat()
    }


    User --|> ObjectRecognition
    ObjectRecognition --|> ObjectProcessing
    ObjectProcessing --|> VirtualObjectsInteraction
    User --|> EducationalMaterialsUsage
    User --|> EducationalOrganizationConnection
    EducationalOrganizationConnection --|> InstitutionMaterialsProvision
    User --|> ChatUsage
    ChatUsage --|> ListManagement

@enduml
```
