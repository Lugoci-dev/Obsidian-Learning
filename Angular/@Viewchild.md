
_El Viewchild nos sirve para tomar una referencia local_


```html
<input type="text" class="form-control" placeholder="Search Gifs" (keyup.enter)="searchTag()" #txtTagInput>
```
_en el ejemplo anterior el #txtTagInput es una referencia local_

```ts
 @ViewChild('txtTagInput')
  public tagInput!: ElementRef<HTMLInputElement>;
```


```ts
public searchTag() {
    const newTag = this.tagInput.nativeElement.value
    console.log({newTag});
  }
```

_El Viewchildren funciona de forma parecida, pero en su caso este devuelve un arreglo de elementos_


[ngStyle]="{display: hasLoaded? '': 'none' }" />