_El @Output es un decorador que se importa de angular/core._

Utilizado para enviar los datos que deseamos desde un componente hijo hasta el componente padre(añadir un nuevo carácter)

```TypeScript
import { Output, EventEmitter } from "@angular/core";
```
_Requiere del EventEmitter para emitir los eventos_

```TypeScript

  @Output()
  public onNewCharacter: EventEmitter<Character> = new EventEmitter();
  //Aca especificamos el tipo de dato que se va a emitir y el nombre de este evento
```

_Luego es necesario emitir dicho evento (Puede ser mediante la interacción con un botón)_

```TypeScript
//este metodo es llamado al pulsarse un boton
public emitCharacter(): void{

    this.onNewCharacter.emit(this.AuxCharacter);
//emitimos el evento pero enviamos por parametros(del tipo especificado) el valor que queremos emitir.
  }
```

_En este caso emitimos AuxCharacter, una variable que deseamos enviar al padre_
```TypeScript
public AuxCharacter: Character = {
    name: '',
    power: 0
  }
```

Al enviar este evento debemos garantizar que nuestro componente padre este 'subscrito' para recibir estos datos.
_Esto lo hacemos en el selector del componente hijo donde hacemos el @output que debe encontrarse en el componente padre _

```html

<dbz-add-character (onNewCharacter)="this.onNewestCharacter($event)">
</dbz-add-character>
```
_Nuestro evento se llama como definimos: onNewCharacter_

Y llamamos una función del componente padre que se encarga de recibir este $event para darle el fin determinado.

Esta función debe recibir como parámetros el mismo tipo de dato que el evento emitido, y realizar las operaciones necesarias una vez recibidos.

```TypeScript

public onNewestCharacter( character: Character){
    this.dbzService.addCharacter(character);
  }
```

En este ejemplo se utiliza un [[Service]] donde tenemos la lógica de nuestro programa (El componente padre hace de controlador).