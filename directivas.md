---
description: >-
  Las Directivas son una parte super importante de Angular, ellas nos permiten
  extender nuestro HTML y darle un toque único que veremos a continuación.
---

# 🧑‍🎨Directivas🧑‍🎨

## ¿Qué es una Directiva?

Una directiva se puede considerar como una parte muy importante del núcleo de Angular. 

Las Directivas extienden la funcionalidad del HTML usando para ello una nueva sintaxis. Con ella podemos usar lógica que será ejecutada en el DOM \(Document Object Model\).

Cada Directiva que usamos tiene un nombre, y determina donde puede ser usada, sea en un elemento, atributo, componente o clase.

Se dividen en tres tipos diferentes:

* Directivas de Atributo
* Directivas de estructurales
* Componentes

![Al extender  nuestro HTML podemos darle toques &#xFA;nicos](.gitbook/assets/angulardirectiva.png)

## Tipos de Directivas



### Directivas de Atributo

Alteran la apariencia o comportamiento de un elemento del DOM. Son usados como atributos de los elementos.

Entre la directivas de atributo, encontramos:

* **ngModel**: Implementa binding
* **ngClass**: permite añadir/eliminar varias clases
* **ngStyle**: permite asignar estilos inline

### Directivas Estructurales

Nos permite añadir, manipular o eliminar  elementos del DOM

En las directivas estructurales podemos encontrar las siguientes:

* **\*ngIf**: Nos permite incluir condicionales de lógica en nuestro código, como por ejemplo evaluar sentencias, hacer comparaciones, mostrar u ocultar secciones de código, y entre las muchas condiciones que deseemos crear, para que se renderice nuestro HTML, cumpliendo la sentencia a evaluar. Con el \*ngIf, podemos evaluar sentencias con un simple If, podemos evaluar el **else**, para que no cumpliéndose la primera condición que se evalúa nuestro código ejecute otra acción en el caso contrario y podemos además incluir el **then**, para que cumpliendose la condición afirmativa \(if\), podamos añadir más flexibilidad a nuestro código incluyéndole un camino afirmativo adicional.

![Ejemplo \*ngIF](.gitbook/assets/carbon-5.png)



* **\*ngFor**: Permite ejecutar bucles, los bucles son los que conocemos en lógica de programación como: for, while, foreach, etc. Con esta directiva estructurar podemos evaluar de acuerdo a nuestra condición n veces.

![Ejemplo de \*ngFor](.gitbook/assets/carbon-4.png)



```text

```

* **ngSwitch**: esta directiva es similar al **\*ngIf**, y es como el switch en lógica de programación. En esta directiva se pueden crear los diferentes casos que deseamos evaluar y cuando se cumple la condición esperada, oculta/muestra el HTML. Nos permite mantener nuestro código más limpio, si necesitamos evaluar varias sentencias.

![Ejemplo ngSwitch](.gitbook/assets/carbon-6.png)

### Directivas de Componente

Las Directivas de Componente son directivas con un Template. Los componentes tienen decoradores "**@Component"**, el componente es un decorador **@Directive** que es extendido con características propias de los _**templates**_.

## ¿Cómo generar una directiva?

Desde el Angular CLI podemos generar una directiva usando el siguiente comando:

```text
ng generate directive <name> [options]
```

En su forma abreviada sería:

```text
ng g d [name]
```

Si usamos un IDE online como **Stackblitz** con solo dar clic derecho sobre la carpeta src, nos aparecerá una opción llamada Angular Generator, si colocamos el mouse sobre esa opción, mostrará varias opciones, entre ellas Directive. Al seleccionarla y colocar un nombre, se genera la directiva.

![Creaci&#xF3;n de directiva usando Stackblitz](.gitbook/assets/screen-shot-2020-05-02-at-11.30.33-pm.png)

![Ejemplo de la directiva generada en Stackblitz](.gitbook/assets/screen-shot-2020-05-02-at-11.32.38-pm.png)

### 

### 

