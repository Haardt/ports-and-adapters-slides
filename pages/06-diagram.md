
```plantuml
@startuml
package "Domain" {
  interface Port1 {
    +operation1()
  }
  interface Port2 {
    +operation2()
  }

  class BusinessService {
    +processData()
  }

  Port1 <|-- BusinessService
  Port2 <|-- BusinessService
}

package "Adapter" {
  class UIAdapter {
    +operation1()
  }
  
  class DBAdapter {
    +operation2()
  }

  UIAdapter --> Port1
  DBAdapter --> Port2
}

@enduml
```
::right::

<br>
<br>
<br>
<div v-click>Primary- or "driving"-Adapter</div>
<arrow v-click x1="480" y1="130" x2="200" y2="100" color="#953" width="2" arrowSize="1" />

<br>
<br>
<br>
<div v-click>Secondary- or "driven"-Adapter</div>
<arrow v-click x1="480" y1="240" x2="345" y2="150" color="#953" width="2" arrowSize="1" />
