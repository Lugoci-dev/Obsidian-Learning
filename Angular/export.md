_Una exportación se hace necesaria si necesitamos utilizar un componente declarado en nuestro modulo. Y se hace cuando nuestro modulo esta siendo importado por otro y es necesario este componente._

```TypeScript

import { NgModule } from '@angular/core';

import { CommonModule } from '@angular/common';

import { MainPageComponent } from './pages/main-page.component';

import { ListComponent } from './components/list/list.component';

import { AddCharacterComponent } from './components/add-character/add-character.component'

import { FormsModule } from '@angular/forms';

import { CounterModule } from '../counter/component/counter.module';

  

@NgModule({

  declarations: [
    MainPageComponent,//este componente agrupa a los demas componentes por esto solo es necesario exportarlo a el
    ListComponent,
    AddCharacterComponent,
  ],

  exports: [
  //Nuestro componente exportado utiliza los demas componentes de el modulo para fprmar la pagina deseada.
    MainPageComponent,
  ],

  imports: [
    CommonModule,
    FormsModule,
    CounterModule,
  ]
})

export class DbzModule { }
```

_Nuestro componente exportado podrá ser utilizado en el modulo que requiere el nuestro por cada uno de sus componentes y se mostrara a través de su selector_

```TypeScript

import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

import { DbzModule } from './dbz/dbz.module';

  

@NgModule({
  declarations: [
    AppComponent,
  ],
  imports: [
  //aca esta nuestro modulo siendo importado
    DbzModule,
  ],
  providers: [
    provideClientHydration()
  ],
  bootstrap: [AppComponent]
})

export class AppModule { }
```

Nuestro componente siendo utilizado en el appComponent del modulo AppModule.

```html

<h1 class="text-danger" style="text-align: center;"> {{title}} </h1>
<hr>

<!-- Nuestro componente siendo utilizado -->
<app-dbz-main-page></app-dbz-main-page>
```