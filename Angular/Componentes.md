_Cada componente son varios archivos .ts .html .css_

```TypeScript

import { Component } from "@angular/core";

  

@Component({

//el selector nos permite representar nuestro componente como un archivo.html

  selector: 'dbz-add-character',

//este es el archivo que se mostrara

  templateUrl: './add-character.component.html',

  styleUrl: './add-character.component.css'

})
export class AddCharacterComponent{

//aqui va el contenido de tu clase

}
```

_'Cada componente puede ser representado por medio de su selector siempre y cuando este sea importado correctamente, o su modulo al q pertenezca.'_



(Utilizando el CLI)
 _"ng g c name_component"_
 ```CMD
 ng g c name_component
```
  _"ng g c path/name"_
  ```CMD
  ng g c file/fileComponents/name-component
```


Comunicación entre componentes: [[@Input]] [[@Output ]]
