# JQUERY MASTERCLASS
---
Esta documentación son apuntes realizados de una masterclass de Jquery y AJAX

Para instalar JQuery basta con ir a la página de Jquery e instalarlo mediante paquetes, descargarlo o usar el CDN mediante enlaces, a la hora de realizar el curso he usado la 3.4.1
```
<script
			  src="https://code.jquery.com/jquery-3.4.1.js"
			  integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU="
			  crossorigin="anonymous">
</script>   
```
Simplemente se añade en el ``` Head ``` de un HTML


# SELECTORS JQUERY
___

### DOCUMENT READY
___
Este método permite verificar cuando la página ha cargado completamente, esté metodo es lo mejor para ejecutar código de Javascript que necesite esperar a que la página haya cargado completamente.

Para usarlo basta con usar la función 

```
$(document).ready(function () {
    console.log("I am ready");
});
```
### ELEMENT SELECTOR
___
Permite seleccionar todos los elementos, por ejemplo un div, el código de ejemplo sería 

```
 $(document).ready(function () {
     $("div").click(function (e) { 
        console.log("All divs selector");
     });
 });
```
### ALL ELEMENTS SELECTOR
___
Selector de todo el contenido de la página 
```
 $(document).ready(function () {
    $("*").click(function () { 
         console.log("All selector");

     });
 });
```

## SELECTOR BY ID
___

Selecciona mediante el ID

``` 
$(document).ready(function () {
    $("#HW").click(function () {
        console.log("Clicked in the ID")
    });
});
```
## SELECTOR BY CLASS
___
Selecciona mediante la clase

```
$(document).ready(function () {
    $(".HW").click(function () {
        console.log("Clicked in the class")
    });
});
```

## COMBINED SELECTORS
___

Permite que distintos selectores ejecuten el mismo bloque de código.
```
$(document).ready(function () {
     $(".HW, #HW").click(function () {
        console.log("Clicked combined")
     });
});
```
## FIRST SELECTOR
___
Solo el primer selector que esté en el código HTML.
```
$(document).ready(function () {
    $("#HW:first").click(function () {
        console.log("Clicked only in the first ID");
    });
});
```

## ODD AND EVEN SELECTOR
___
Solo aplica el código en función de si el selector es par o impar, odd es impar, even es par. Empieza a contar desde 0

```
$(document).ready(function () {
    $(".divclass:odd").click(function () {
        console.log("Clicked only in the odd elements");
    });
});
```
```
$(document).ready(function () {
    $(".divclass:even").click(function () {
        console.log("Clicked only in the even elements");
    });
});


```

## THIS SELECTOR
___
Muestra los datos del selector

` console.log ($(this)); `

Oculta lo que contenga el selector
` $(this).hide();`
