
_Siempre que sea necesario determinadas características como decoradores etc. será necesario realizar algunas importaciones_

Las importaciones que suelen ser de componentes o interfaces es necesario para poder utilizarlas que estén igualmente bien importadas.

```TypeScript

//importaciones necezarias para usar ciertas caracteristicas
import { NgModule } from '@angular/core';

import { CommonModule } from '@angular/common';

import { FormsModule } from '@angular/forms';

//Modulo creado
import { CounterModule } from '../counter/component/counter.module';

  

@NgModule({

  declarations: [],
  exports: [],

  imports: [
//Modulos o dependencias preconfiguradas
    CommonModule,
    FormsModule,

//Importacion dde un modulo creado por mi
    CounterModule,
  ]
})

export class DbzModule { }
```

{ NgModule } from '@angular/core'    ___se utiliza para los decoradores de los modulos

{ CommonModule } from '@angular/common'    ___necesario para utilizar la propiedad de [ngClass] = ""

import { FormsModule } from '@angular/forms'    ___permite utilizar las propiedades de [(ngModel)] = ""

