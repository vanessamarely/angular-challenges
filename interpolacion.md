---
description: La interpolación es el concepto mas básico que se emplea en Angular.
---

# 🧔🏻 Interpolación {{}} 🧔🏻

## ¿Qué es la interpolación?

![](.gitbook/assets/angular-bigote.png)

La interpolación es su definición más básica nos permite obtener la información  definida en la lógica y mostrarla en el HTML.

En Interpolación se utiliza la sintaxis `{{ valor }}`

```markup
<h3>2 + 2 es igual a {{2 + 2}}</h3>
```

{% hint style="info" %}
 se usan las dobles llaves {{}}, que visualmente se parece a un mostacho o bigote.
{% endhint %}

A la interpolación, se le conoce como interpolación de cadenas, también conocida en inglés como "string interpolation".

A su sintaxis se le conoce como "moustache syntax" o sintaxis de bigote

Lo que se coloca entre las dobles llaves son llamadas expresiones. Podemos crear expresiones simples y complejas.

Cualquier expresión al final de cuentas se convertirá en una cadena y eso es lo que se colocará en la vista del componente.

Podemos ver expresiones con operaciones matemáticas.

```text
{{ 2 + 2 }}
```

Expresiones con operadores lógico de negación:

```text
{{ !valor }}
```

Expresiones que son devueltas en un método de componente. Lo que devuelva ese método es lo que se colocará en el template.

```text
{{ metodoComponente() }}
```

## Reto Básico

Vamos a crear una mini galería dónde usaremos el concepto de interpolación. 

Para nuestra App vamos a seguir los siguientes pasos:

### Paso 1

Crearemos nuestro "**Hello Angular**", usando un IDE online como **Stackblitz**, podemos ver la guía de **Stackblitz** en la sección de "Guías útiles" .

Vamos a la página de **stackblitz.com** y creamos nuestra App de Angular.

![P&#xE1;gina inicial de Stackblitz](.gitbook/assets/screen-shot-2019-08-26-at-8.04.27-pm.png)

![Creamos nuestra App de Angular](.gitbook/assets/screen-shot-2019-08-26-at-8.06.10-pm.png)

![Hello Angular](.gitbook/assets/screen-shot-2019-08-26-at-8.10.54-pm.png)

### Paso 2

Vamos a ir al archivo "**app.component.html**", seleccionamos el contenido y lo borramos.

![Seleccionamos el contenido y lo borramos](.gitbook/assets/screen-shot-2019-08-26-at-8.15.11-pm.png)

### Paso 3

En el archivo **app.component.html** vamos a colocar unas etiquetas para los títulos y una para una imagen. 

Vamos a incluir en nuestra imagen la siguiente url de un gif animado: [https://cdn2.thecatapi.com/images/49f.gif](https://cdn2.thecatapi.com/images/49f.gif)

![](https://cdn2.thecatapi.com/images/49f.gif)

Nos queda nuestro archivo con el siguiente código:

{% code-tabs %}
{% code-tabs-item title="app.component.html" %}
```text
<h1>Interpolación</h1>
<h2>Reto básico</h2>
<img src="https://cdn2.thecatapi.com/images/49f.gif" />
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Paso 4

Hemos añadido nuestra imagen, pero la idea es crear una mini galería con varias imágenes. Podemos duplicar la etiqueta de la imagen y tendríamos algo como esto:

![Duplicamos la etiqueta &amp;lt;img /&amp;gt;](.gitbook/assets/screen-shot-2019-08-26-at-8.35.03-pm.png)

Usaremos la interpolación para la url de la imagen, entonces solo dejaremos una etiqueta de imagen y crearemos una variable en el archivo **app.component.ts**, llamada **img**  donde pondremos la ruta de la imagen.

{% hint style="info" %}
No modifiques nada más del contenido de **app.component.ts**, la sintaxis que ves en ese archivo es la básica de Angular.
{% endhint %}

Nos quedará un código como el siguiente:

{% code-tabs %}
{% code-tabs-item title="app.component.ts" %}
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'my-app',
  templateUrl: './app.component.html',
  styleUrls: [ './app.component.css' ]
})
export class AppComponent  {
  name = 'Angular';
  img = 'https://cdn2.thecatapi.com/images/49f.gif';
}

```
{% endcode-tabs-item %}
{% endcode-tabs %}

Usaremos una API de gifs animados para tener más gifs animados en nuestra etiqueta **&lt;img /&gt;**, colocaremos a nuestra variable **img** la url del API: [https://thecatapi.com/api/images/get?format=src&type=gif](https://thecatapi.com/api/images/get?format=src&type=gif?results_per_page=)

![](.gitbook/assets/screen-shot-2019-08-26-at-8.48.18-pm.png)

### Paso 5

Asignaremos en nuestra etiqueta **&lt;img /&gt;** la url almacenada en nuestra variable.

Cambiaremos el texto de la variable **name** y pondremos en su lugar el texto Interpolación y lo incluiremos en uno de los títulos.

{% code-tabs %}
{% code-tabs-item title="app.component.html" %}
```markup
<h1>{{name}}</h1>
<h2>Reto básico</h2>

<img src="{{img}}" />
```
{% endcode-tabs-item %}
{% endcode-tabs %}

![Agregamos las variables en el HTML](.gitbook/assets/screen-shot-2019-08-26-at-9.17.29-pm.png)

Duplicamos la etiqueta &lt;img /&gt; 6 veces para tener nuestra galería

