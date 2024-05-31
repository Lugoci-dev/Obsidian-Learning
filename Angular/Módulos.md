(Forma manual)
_Cada modulo es un solo archivo.ts_
```TypeScript

//importacione de dependencias
import { NgModule } from '@angular/core';
import { CommonModule } from '@angular/common';
import { FormsModule } from '@angular/forms';


//importacion de componentes
import { MainPageComponent } from './pages/main-page.component';

import { ListComponent } from './components/list/list.component';

import { AddCharacterComponent } from './components/add-character/add-character.component'


//importacion de un modulo
import { CounterModule } from '../counter/component/counter.module';


//Cada importación, o declaración debe ser correctamente importada de donde se encuentra.

@NgModule({

  declarations: [
//aqui se llaman los componentes que se usaran en el modulo.

    MainPageComponent,
    ListComponent,
    AddCharacterComponent,
  ],
  exports: [
//ya que el modulo será visible en el appModule debemos exportar la pagina principal que queremos ver.

    MainPageComponent,

  ],
  imports: [
//aquí deben realizarse todas las importaciones necesarias para ser usadas dentro de los componentes.

    CommonModule,
    FormsModule,
    CounterModule,
  ]
})

export class DbzModule { }

// finalmente exportamos nuestra clase para que sea visible en los demás módulos.
``` 

Una vez que un modulo tiene importado varios componentes es posible que entre ellos puedan hacer uso de sus selectores.

Aunque para usar el selector de alguno de estos en un modulo que importe el nuestro será necesario [[export]] dicho componente.



(Utilizando el CLI)
 _"ng g m name_module"_
  _"ng g m path/name"_


