_El @Input es un decorador que se importa de angular/core._

```TypeScript
import { Output } from "@angular/core";
```

_Se utiliza para darle valor a determinado objeto(variable) en el componente deseado desde el componente padre_

```TypeScript
@Input()
  public characterList: Character[] = [{
      name: 'Prueba',
      power: 0,
    }
  ];
```

_Este "characterList" esta recibiendo un arreglo de "Characteres" dese el componente padre_
Esto se hace mediante corchetes en el selector en el HTML [__donde llamamos nuestro componente.__]

```html
<dbz-list [characterList]="characters"></dbz-list>
```

_este "characterList" es el mismo characterList en nuestro @Input y se le esta asignando como valor "characters"_ que debe ser un arreglo de "Characteres" existente en el componente padre.


De este modo enviamos datos desde nuestro componente padre hacia nuestro componente hijo, utilizando el @Input.