# HTML

## ¿Qué es HTML?
HTML significa Lenguaje de Marcado para Hipertextos (HyperText Markup Language). Es el elemento de construcción más básico de una página web y se usa para crear y representar visualmente una página web. Determina el contenido de la página web, pero no su funcionalidad. Otras tecnologías distintas de HTML son usadas generalmente para describir la apariencia/presentación de una página web (CSS) o su funcionalidad (JavaScript).

Un lenguaje de marcas utiliza etiquetas para definir estructuras y mostrar distintos tipos de datos como pueden ser textos, imagenes, videos, etc.

¿e Hipertexto?

HiperTexto se refiere a enlaces que conectan una página Web con otra, ya sea dentro de una página web o entre diferentes sitios web. Los vínculos son un aspecto fundamental de la Web. Al subir contenido a Internet y vincularlo a páginas de otras personas, te haces participante activo de esta Red Mundial.

## Historia de HTML
HTML fue inventado por Tim Berners-Lee, un físico del instituto de investigación CERN en Suiza. Se le ocurrió la idea de un sistema de hipertexto basado en Internet.

Publicó la primera versión de HTML en 1991, que constaba de 18 etiquetas HTML. Desde entonces, cada nueva versión del lenguaje HTML viene con nuevas etiquetas y atributos (modificadores de etiqueta) para el marcado.

Según la Referencia de elementos HTML de Mozilla Developer Network, actualmente hay 140 etiquetas HTML, aunque algunas de ellas ya están obsoletas (no son compatibles con los navegadores modernos).

Debido a un rápido aumento de la popularidad, HTML ahora se considera un estándar web oficial. Las especificaciones de HTML son mantenidas y desarrolladas por el World Wide Web Consortium (W3C).

La actualización más importante del lenguaje fue la introducción de [HTML5](https://es.wikipedia.org/wiki/HTML5)en el 2014. Se agregaron varias etiquetas semánticas nuevas al marcado, que revelan el significado de su propio contenido, como <article>, <header> y <footer>.

## ¿Cómo funciona HTML?
Los documentos HTML son archivos que terminan con una extensión .html o .htm. El navegador lee el archivo HTML y muestra su contenido para que los usuarios de Internet puedan verlo.

Por lo general, el sitio web promedio incluye varias páginas HTML diferentes. Por ejemplo: las páginas de inicio, las páginas de acerca de y las páginas de contacto, todas tendrán documentos HTML separados.

Cada página HTML consta de un conjunto de etiquetas (también denominadas elementos), a las que te puedes referir como los componentes básicos de las páginas web. Crean una jerarquía que estructura el contenido en secciones, párrafos, encabezados y otros bloques de contenido.

La mayoría de los elementos HTML tienen una apertura y un cierre que utilizan la sintaxis:

```html
<tipoDeEtiqueta>
  Bienvenides a HTML!
</tipoDeEtiqueta>
```

## Estructura
Cuando trabajamos con HTML, utilizamos estructuras de código simples (etiquetas y atributos) para marcar una página web.

### Estructura de una etiqueta o tag
Una etiqueta actúa como un contenedor y describe los datos o información que contienen entre la etiqueta de apertura y la de cierre.

```html
<tipoDeEtiqueta>Acá va el contenido</tipoDeEtiqueta>
```

**Etiquetas sin contenido:**
* Algunas etiquetas no tienen contenido y funcionan como placeholder (un lugar donde vamos a poner algo).
* Este tipo de etiquetas utilizan la apertura y cierre en una sola estructura
* Un ejemplo de este tipo de etiquetas es el contenedor para insertar una imagen.

```html
<img />
```

**Ejemplo de un elemento con otro elemento:**
En el siguiente ejemplo tenemos una etiqueta (no sabemos de qué tipo) que tiene como contenido un texto (HTML rocks!) y una imagen que por ahora no sabemos cual es.

En este ejemplo vemos que el texto y la imagen tienen un márgen izquierdo para visualizar de forma rápida y fácil que son contenido del elemento llamado tipoDeEtiqueta. Esta técnica se conoce como [identación o identado](https://es.wikipedia.org/wiki/Indentaci%C3%B3n) y es una buena práctica para evitar tener problema a la hora de armar documentos con estructuras más complejas.

```html
<tipoDeEtiqueta>
  HTML rocks!
  <img />
</tipoDeEtiqueta>
```

## Estructura de un documento HTML

Todo documento HTML va a tener las siguientes estructuras principales.

* Declaración de tipo de documento (doctype)
* Etiqueta HTML que actúa como elemento principal de nuestro documento
* Un encabezado para agregar información adicional sobre la página (head)
* Un cuerpo con el contenido de nuestro documento (body)

#### DOCTYPE:

Dado que existen distintas versiones de HTML vamos a comenzar nuestro documento declarando la versión que vamos a utilizar así el browser interpreta el resto del contenido de forma correcta.

El browser puede renderizar el documento sin esta declaración pero nosotros siempre lo vamos a definir para evitarnos problemas y sobre todo para tener un documento bien formado.

**DOCTYPE versión HTML5:**
```html
<!DOCTYPE html>
```

#### HTML
Esta etiqueta es el elemento de más alto nivel que encierra toda la página HTML.

```html
<html></html>
```

#### HEAD
Dentro de la etiqueta HTML vamos a tener una sección donde podemos describir cosas sobre nuestra página. Esta sección se llama HEAD (cabeza) y no va a ser visible en el documento ya que es de uso interno del browser.

```html
<head></head>
```

#### BODY
* El browser va a renderizar todo el contenido que esta dentro de este elemento. Podemos decir que es todo lo que vemos en pantalla.

```html
<body></body>
```

**lo vamos armando? ;)**

```html
<html>
  <head>  
  </head>
  <body>
  </body>
</html>
```

#### Title
* El contenido de la etiqueta title se ve en la parte superior del browser o como contenido de los tabs(solapa).
```html
<head>
  <title>Título de nuestro documento y se ve en el tab del browser.</title>
</head>
```

#### La codificación (charset)
La codificación especifica cómo se guarda un archivo. Es lo que determina la forma en la que se van a mostrar los caracteres especiales (acentos, caracteres japoneses y chinos, caracteres arábigos, etc.)

Hay varias técnicas de codificación con nombres raros que se usan en función del idioma: ISO-8859-1, OEM 775, Windows-1253, etc. No obstante, actualmente solo se debería usar una: UTF-8. ¡Este método de codificación permite que todos los símbolos de todos los idiomas del mundo se muestren virtualmente sin ningún problema! Esta es la razón por la que indiqué **utf-8** en esta etiqueta.

```html
<html>
  <head>
    <title>La codificación</title>
    <meta charset="utf-8" >
  </head>
  <body>
  </body>
</html>
```
#### Práctica
[Ejercicio 1](../ejercicios/consignas/html/ej01.md)

## Etiquetas de texto
###Títulos
* En HTML tenemos 6 niveles de etiquetas para los títulos de nuestro documento o secciones.
* Los títulos utilizan la etiqueta **h** y el número de tipo de título.
* El browser por defecto muestra la diferencia entre los títulos utilizando una tipografía más grande para el H1 y la más pequeña para el H6.
* Conceptualmente debemos utilizar los títulos en orden respetando su jerarquía. (primero el h1, después el 2, etc)

**Ejemplos:**
```html
<h1>Título Principal del documento</h1>
<h2>Título secundario</h2>
<h3>Título 3</h3>
<h4>Título 4</h4>
<h5>Título 5</h5>
<h6>Título 6</h6>
```

### Etiqueta párrafo
Para agregar párrafos y textos tenemos una etiqueta especial que se llama **p**
* El párrafo es un **elemento en bloque** y es por esto que el browser por defecto nos va a mostrar un párrafo por linea.

**Ejemplo**
```html
<p>Contenido de mi párrafo.</p>
<p>Contenido de          mi párrafo.</p> (sólo va a mostrar un espacio)
```

**Se pueden titular párrafos? claaaaro!**
```html
<p>
  <h2>Párrafo #1</h2>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque lacinia purus quis dolor condimentum tincidunt. Pellentesque pretium vulputate consequat. Vestibulum nisl risus, pharetra eu dolor eget, sollicitudin dapibus dolor.
</p>

<p>
  <h2>Párrafo #2</h2>
  Ut quis venenatis lectus. Aliquam vitae diam a neque condimentum condimentum eu consequat mi. Suspendeger tempus finibus metus, ac posuere eros maximus at.
</p>
```
* Observen que los H2 tienen un espacio adelante. Aunque esto no es obligatorio y no afecta a la forma en la que se muestra la página hace que el código fuente sea más legible. Esto se llama indentation (sangría). Se consigue apretando la tecla TAB.

### Salto de línea (br)
* **br** inserta un salto de línea simple

**Ejemplo:**
```html
<p>Contenido de nuestro párrafo en una línea <br />
Contenido de nuestro párrafo en otra línea</p>
<br />
<br />
Podemos utilizar el salto de linea <br />
en cualquier lado de nuestro documento.
```

### Línea divisora (hr)
* **hr** define una línea horizontal a manera separador de texto

**Ejemplo:**
```html
<h1>Título principal de nuestro documento</h1>
<h2>Título secundario</h2>
<p>Primer contenido</p>
<hr />
<p>Segundo contenido</p>
```

**Formato de texto**
Existen algunas etiquetas de HTML que nos permiten describir cómo es el texto del
documento:

```html
<b>Negrita SIN importancia semántica</b>
<strong>Negrita CON importancia semántica</strong>

<i>Itálica o cursiva SIN importancia semántica</i>
<em>Itálica o cursiva CON importancia semántica</em>

<small>Define texto pequeño</small>

<sub>Texto como subíndice</sub>
<sup>Texto como superíndice</sup>

<del>Texto tachado</del>
<mark>Texto resaltado</mark>
```

#### Práctica
[Ejercicio 2](../ejercicios/consignas/html/ej02.md)

## Listas
Las listas normalmente nos permiten organizar el texto y ordenar la información.
Vamos a descubrir dos tipos de listas aquí:

* listas no ordenadas o listas con viñetas;
* listas ordenadas o listas enumeradas.

### Listas no ordenadas
Una lista no ordenada tiene esta apariencia:

* Fresas
* Frambuesas
* Cerezas

Se utiliza la etiqueta **ul** para establecer que es una lista del tipo desordenada o Unordered
List y cada item estará encerrado en elementos **li**

**Ejemplo:**
```html
<ul>
  <li>Manzanas</li>
  <li>Bananas</li>
  <li>Peras</li>
</ul>
```

### Listas ordenadas
Una lista ordenada funciona de la misma forma únicamente cambia la etiqueta por **ol** (Ordered list). Aquí sí el orden en el que se colocan los elementos en la lista es importante ya que se enumeran, por lo tanto el primer **li** será el elemento número 1, el segundo será el elemento número 2, etc.

**Ejemplo:**
```html
<ol>
  <li>Comprar café</li>
  <li>Prender máquina</li>
  <li>Codear</li>
</ol>
```

**Nota:** Se pueden crear listas complejas anidando listas. Para eso debes abrir una segunda etiqueta **ul** u **ol** y poned dentro sus elementos **li**.
Si cerrás las etiquetas en el orden correcto no tendréis ningún problema.

#### Práctica
[Ejercicio 3](../ejercicios/consignas/html/ej03.md)
[Ejercicio 4](../ejercicios/consignas/html/ej04.md)
[Ejercicio 5](../ejercicios/consignas/html/ej05.md)

## Enlaces
Un enlace es un texto en el que hacés click para ir a otra página. Podés crear un enlace para ir de la página a.html a la página b.html, pero también podés crear un enlace a otro sitio web, por ejemplo http://www.google.com. Ambos casos funcionan de la misma forma.

Para insertar un enlace se utiliza la etiqueta **a**. Sin embargo, necesita un atributo, **href**, que indica la página a la que debería llevar el enlace. Entre la etiqueta de apertura y cierre ponemos el contenido del link, que puede ser también una imagen.

Por ejemplo el código que está a continuación lleva a Google, localizado en la dirección http://www.google.com

```html
<a href="http://www.google.com"></a>
```

Este tipo de enlace se llaman **enlaces absolutos** debido a que muestran la dirección completa.
Si en cambio quisieramos linkear con un archivo local con esta misma lógica deberíamos hacerlo de la siguiente manera:

```html
<a href="c:\Usuarios\Estefania\avatar.pdf">Mi foto</a>
```
Ahora bien, cómo vinculo con otro documento html que aún no tiene una "dirección web" que empiece con **http://** como la mayoría de los sitios web? La respuesta es con **enlaces relativos**.

Este tipo de rutas está definida por la relación que tienen los documentos. Algunas relaciones que pueden darse son las siguientes:

**a.html**
```html
<a href="b.html">Ir a la página B</a>
<!-- a.html y b.html se encuentran en la MISMA carpeta -->
<a href="../b.html"></a>
<!--a.html y b.html se encuentran en carpetas diferentes; b.html se encuentra en la carpeta raíz, es decir, una carpeta "más arriba" en la estructura de árbol -->
<a href="contenido/b.html"></a>
<!-- b.html se encuentra en una subcarpeta -->
```

**Un enlace que muestra una descripción emergente**
Se puede utilizar el atributo **title** que muestra una descripción emergente cuando coloques el curso sobre el enlace. Este atributo es opcional.

La descripción emergente puede ser útil para proporcionar información a los visitantes incluso antes de que hayan hecho click sobre el enlace.

```html
<a href="https://ada.com.ar" title="Aprende a programar con la carrera de Ada">Ada</a>
```

**Un enlace que abre a una ventana nueva**
Un enlace se puede obligar a abrir a una nueva ventana. Para hacer esto, se añade el atributo **target="_blank"** a la etiqueta **a**

**Ejemplo**
```html
<a href="https://ada.com.ar" target="_blank">Ir a Ada</a>
```
[Ejercicio 6](../ejercicios/consignas/html/ej06.md)
[Ejercicio 7](../ejercicios/consignas/html/ej07.md)


## imagenes

En HTML podemos utilizar la etiqueta **img** como contenedor de una imagen.
Es una etiqueta huérfana (como <br />). Esto quiere decir que no tienes que introducir dos etiquetas como en el caso de la mayoría de etiquetas que hemos visto hasta ahora. De hecho, no tenemos que definir una porción de texto; lo único que queremos es colocar una imagen en un punto específico.

La etiqueta debe ir acompañada de dos atributos obligatorios:

* **src**: que indica la ubicación en la que quieres insertar la imagen. Puedes incluir una ruta absoluta (e.g.http://www.website.com/flor.png) o una ruta relativa (que es lo que suele hacerse). Así que si la imagen está en la subcarpetaimagenes, tienes que introducir: src="imagenes/flor.png"

* **alt**: que significa "texto alternativo". Un texto alternativo a la imagen, en otras palabras, un texto corto que describe lo que contiene la imagen, debe indicarse siempre. Este texto se mostrará en lugar de la imagen si esta última no se puede descargar (esto ocurre), o en los navegadores de personas con discapacidad visual que lamentablemente no pueden "ver" la imagen. También ayuda a los robots de motores de búsqueda a buscar imágenes. Para la flor, por ejemplo, se debería escribir lo siguiente: ´ alt="Una flor"´

**Ejemplo**
```html
<img src="mifoto.jpg" alt="mi foto personal"/>
```

Utilizando los atributos **height** para la altura y **width** para el ancho podemos establecer el tamaño que queremos que tenga el contenedor. Podemos establecer un número como valor de estos atributos y la unidad de medida es en pixeles

```html
<img src="mifoto.jpg" height="300" width="300" />
```

### Foto con detalle
* Muchas veces necesitamos mostrar una imagen con un detalle, para esto HTML5 incorpora los elementos **figure** y **figcaption**
* Como contenido de **figure** podemos poner una imagen o más imagenes
* Utilizamos **figcaption** para establecer el detalle de la/s imagen/es

**Ejemplo:**
```html
<figure>
  <img src="pikachu.png">
  <figcaption>El Pokemon de Ash Ketchum</figcaption>
</figure>
```

>**Hay un formato apropiado para cada imagen**
> * **JPEG**: para fotos;
> * **PNG**: para todas las demás ilustraciones;
> * **GIF**: similar a PNG, con un número de colores más limitado, pero puede ser animado

## Etiquetas genéricas
Las etiquetas genéricas son etiquetas que no tienen ningún significado semántico.

De hecho, todas las otras etiquetas HTML tienen un significado: <p> significa "Párrafo", <h2> significa "Subtítulo", etc.
A veces se necesita utilizar etiquetas genéricas (también llamadas **etiquetas de finalidad general**) ya que ninguna de las otras etiquetas es apropiada. Lo que más a menudo utilizas para construir tu diseño son las etiquetas genéricas ya que actúan como contenedores de otras etiquetas.

Estas etiquetas son los **divs** y **spans**!

Copiá el ejemplo que sigue...
```html
<div style="background-color:#ffcc00">
  <p>Soy el párrafo del div #1<p>
</div>
<div style="background-color:red">
  <p>Soy el párrafo del div #2<p>
</div>

<span style="background-color:#ffcc00">
  <p>Soy el párrafo del span #1<p>
</span>
<div style="background-color:red">
  <p>Soy el párrafo del span #2<p>
</div>
```

Qué notaste? Sí, los divs y los spans se visualizan diferente.

> Cada elemento HTML tiene un valor de visualización por defecto dependiendo de qué tipo de elemento que es. Un elemento en bloque siempre empieza en una nueva línea y ocupa todo el ancho disponible, mientras que los elementos en linea no inician una nueva línea y sólo ocupan el ancho necesario


## Formularios
Cualquier página HTML puede mejorarse con formularios interactivos que piden al visitante que rellene información: introducir texto, seleccionar opciones, confirmar con un botón, etc.

La etiqueta principal los formularios es la etiqueta **form**, y especifica su comienzo y su fin.
Esta lleva dos atributos:
* **method**: especifica cómo se van a enviar los datos. Hay dos manera de enviar datos a la Web:
  * **method="get"**: la información se enviará a la dirección de la página (en la url, ej: nombre=valor&apellido=valor). Este método normalmente es menos adecuado, ya que se limita a 255 caracteres.
  * **method="post"**: es el método más usado en formularios puesto que permite que se envíe un montón de información. Los datos introducidos en el formulario no van a través de la barra de direcciones
* **action**: es la dirección de la página o programa que va a procesar los datos del formulario

```html
<form action="tratamiento_datos.html" method="post">
  Mi form
</form>
```

### Inputs

Para insertar un campo de texto en una línea, vamos a utilizar la etiqueta **input**. Existen diferentes tipos de inputs y cada uno de ellos tiene una funcionalidad distinta. Lo que cambia en cada uno de ellos es el atributo **type**.

##### Texto
* Se utilizan para ingresar una línea de texto como puede ser un nombre, apellido, email, dirección, etc
* Para definir este tipo de input utilizamos el **type** text
* Con el atributo **name** definimos el nombre de la variable

**Ejemplo:**
```html
<form>
  <input type="text" name="apellido" />
</form>
```

**Algunos atributos adicionales**

Puedes añadir varios atributos adicionales a la etiqueta **input** para personalizar su funcionamiento:
  * Aumentar el tamaño del campo con **size**
  * Limitar la cantidad de caracteres que puede ingresar un usuario mediante **maxlength**
  * Prellenar el campo con un valor por defecto con **value**
  * Puedes dar algún indicio de los contenidos del campo mediante **placeholder**. Esta indicación desaparece a medida que el usuario escriba.

  **Ejemplo:**
  ```html
  <form>
    <input type="text" name="username" placeholder="Nombre de usuario" size="30" maxlength="10"/>
  </form>
  ```

##### Contraseña
Existe el campo de contraseña donde no puede verse en pantalla los caracteres que se escriban. Para crear este tipo de entrada, se utiliza el atributo **type="password"**

```html
<form action="tratamiento_datos.html" method="post">
  <label for="username"> Nombre de usuario:</label>
  <input type="text" name="username" id="username">

  <br>
  <label for="pass">Contraseña</label>
  <input type="password" name="pass" id="pass">
</form>
```

> Hacé click en el texto "Nombre de usuario": verás que el cursor se sitúa automáticamente en el campo de texto correspondiente

##### Etiquetas
Para comunicarle al usuario qué valor tiene que ingresar en cada campo podemos utilizar el elemento **label** o etiqueta.

```html
<form action="tratamiento.php" method="post">
  <label>Nombre usuario:</label>
  <input type="text" name="username">
</form>
```  

Para enlazar la etiqueta con el campo, se le tiene que dar un atributo **for**, que tenga el mismo valor de un atributo **id** del input.

```html
<form action="tratamiento.php" method="post">
  <label>Nombre usuario:</label>
  <input type="text" name="username">
</form>
```

##### Numero
Este campo se utiliza para escribir un número entero. El campo normalmente se muestra con unas pequeñas flechas para cambiar el valor.

```html
<form action="tratamiento.php" method="post">
  <label for="edad">Edad:</label>
  <input type="number" name="edad" id="edad">
</form>
```
Podés personalizar la manera en la que funciona el campo con los siguientes atributos:
  * **min**: valor mínimo permitido
  * **max**: valor máximo permitido
  * **step**: es el desplazamiento. Si especificas un "step" de 2, el campo sólo aceptará valores de 2 en 2 (por ejemplo: 0, 2, 6, etc.).

##### Rango
El tipo **range** se utiliza para seleccionar un número con un cursor (también llamado un ***slider***).

```html
<form class="" action="index.html" method="post">
  <input type="range">
</form>
```

Podés utilizar de nuevo los atributos **min**, **max** y **step** para limitar los valores disponibles.

## Opciones
HTML incluye un montón de opciones que pueden usarse en el formulario. Son elementos que requieren que el visitante elija a partir de una lista de posibilidades. Son las siguientes:

  * casillas de verificación;
  * campos de opciones;
  * listas desplegables;

  **Checkboxes (casillas de verificación)**
  Permite que el usuario seleccione/deseleccione múltiples opciones:

  ```HTML
    Hobbies:
    <form action="index.html" method="post">
      <input type="checkbox" name="mandalas" id="mandalas">
      <label for="mandalas">Pintar mandalas</label>
      <br>

      <input type="checkbox" name="correr" id="correr">
      <label for="correr">Correr</label>
      <br>

      <input type="checkbox" name="codear" id="codear">
      <label for="codear">Codear</label>
    </form>    
  ```
> También podés tener una casilla marcada por defecto con el atributo **checked**.
>Todos los aributos normalmente tienen un valor. Sin embargo, en ese caso añadir un valor no es necesario: la presencia del atributo es suficiente para hacer que el browser entienda que la casilla tiene que estar marcada.

**Radio buttons (campos de opciones)**
Los campos de opciones te permiten elegir una (y solamente una)opción de una lista de posibilidades. De alguna manera, parecen casillas de verificación pero hay una dificultad adicional: tienen que estar organizadas como grupos. Aunque las opciones en el mismo grupo tienen el mismo **name**, cada opción tiene que tener un **value** diferente.

La etiqueta que se utiliza es **input** con el valor **radio** en el atributo **type**.

```html
<form method="post" action="tratamiento.php">
        <label>Indica el grupo de edad al que perteneces:</label>
       <input type="radio" name="edad" value="menos15" id="menos15" /> <label for="menos15">Menos de 15 años</label><br />
       <input type="radio" name="edad" value="entre15-25" id="entre15-25" /> <label for="entre15-25">Entre 15 y 25 años</label><br />
       <input type="radio" name="edad" value="entre25-40" id="entre25-40" /> <label for="entre25-40">Entre 25 y 40 años</label><br />
       <input type="radio" name="edad" value="mas40" id="mas40" /> <label for="mas40">Incluso mayor que eso?</label>
</form>
```

Si tenés dos campos de opciones diferentes, tenés que dar un **name** único a cada grupo, de esta forma:

```html
<form method="post" action="tratamiento.php">
       <label>Indica el grupo de edad al que perteneces:</label>
       <input type="radio" name="edad" value="menos15" id="menos15" /> <label for="menos15">Menos de 15 años</label><br />
       <input type="radio" name="edad" value="entre15-25" id="entre15-25" /> <label for="entre15-25">Entre 15 y 25 años</label><br />
       <input type="radio" name="edad" value="entre25-40" id="entre25-40" /> <label for="entre25-40">Entre 25 y 40 años</label><br />
       <input type="radio" name="edad" value="mas40" id="mas40" /> <label for="mas40">¿Incluso mayor?</label>

       <label>¿En qué continente vives?</label>
       <input type="radio" name="continente" value="europa" id="europa" /> <label for="europa">Europa</label><br />
       <input type="radio" name="continente" value="africa" id="africa" /> <label for="africa">África</label><br />
       <input type="radio" name="continente" value="asia" id="asia" /> <label for="asia">Asia</label><br />
       <input type="radio" name="continente" value="america" id="america" /> <label for="america">América</label><br />
       <input type="radio" name="continente" value="australia" id="australia" /> <label for="australia">Australia</label>
</form>
```

**Listas desplegables (select)**
Las listas desplegables son otra manera elegante de seleccionar una opción a partir de varias posibilidades. Funcionan de una manera ligeramente distinta. Vamos a utilizar la etiqueta **<select> </select>**, que especifica el comienzo y el final de la lista desplegable. Añadimos el atributo **name** a la etiqueta para darle un nombre a la lista.

Después, dentro de la etiqueta **<select> </select>**, insertamos varias etiquetas **<option> </option>** (una para cada opción posible). Añadimos un atributo value a cada uno de ellas para identificar lo que el visitante ha elegido.

```html
<form method="post" action="tratamiento.php">
      <label for="pais">¿En qué país vivís?</label><br />
       <select name="pais" id="pais">
           <option value="Brasil">Brasil</option>
           <option value="Argentina">Argentina/option>
           <option value="Uruguay">Uruguay</option>
           <option value="Bolivia">Bolivia</option>
           <option value="España">España</option>
           <option value="Chile">Chile</option>
           <option value="Ecuador">Ecuador</option>
           <option value="Corea del Sur">Corea del sur</option>
       </select>
</form>
```

**El botón de envío**
Así que ahora lo que nos queda por hacer es crear el botón de envío. De nuevo, la etiqueta **<input />** viene a nuestro rescate. Hay cuatro versiones:

* type="submit": el botón de envío principal del formulario. Este es el que usarás más a menudo. El usuario será redireccionado a la página especificada en el atributo action del formulario.

* type="reset": restablece el formulario

* type="image": equivalente al botón submit, pero esta vez mostrado como una imagen. Añade el atributo src para especificar la URL de la imagen.

* type="button": botón genérico, que no tendrá efecto alguno (por defecto). En general, este botón se maneja en JavaScript para desarrollar acciones en la página.

Para crear un botón de envío, entonces escribimos, por ejemplo:

```html
<input type="submit" value="Enviar" />
```

Cuando haces clic en el botón **«Enviar»**, entonces el formulario te lleva a la página especificada en el atributo **action**

.

## Evolución de HTML. ¿Qué diferencia hay entre HTML y HTML5?
Desde sus inicios, HTML ha pasado por una evolución increíble. W3C publica constantemente nuevas versiones y actualizaciones, mientras que los hitos históricos también obtienen nombres particulares.

HTML4 (hoy en día comúnmente denominado “HTML”) fue publicado en 1999, mientras que la última versión importante se publicó en 2014. Con el nombre de HTML5, la actualización ha introducido muchas características nuevas en el lenguaje.

Una de las características más esperadas de HTML5 es el soporte nativo para la incorporación de audio y video. En lugar de usar Flash Player, podemos simplemente incrustar videos y archivos de audio en nuestras páginas web utilizando las nuevas etiquetas **<audio> </audio>** y **<video> </video>**. También incluye soporte incorporado para gráficos vectoriales escalables (SVG) y MathML para fórmulas matemáticas y científicas.

HTML5 introdujo algunas mejoras semánticas también. Las nuevas etiquetas semánticas le informan a los navegadores sobre el significado del contenido, lo cual beneficia tanto a los lectores como a los motores de búsqueda.

Las etiquetas semánticas más populares son `<article> </article>`, `<section> </section>`, `<aside> </aside>`,`<header> </header>`y `<footer> </footer>`.
