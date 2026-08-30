 pestañas de un cuadro de dialogo,, cada tab.

# Etiquetas Semanticas para (SEO) Search Engine Optimization aporta Accesibilidad

## - Etiquetas de Bloque HTML

#### 1- Article : Sirve para definir partes con suficiente importancia como para considerarse una entidad destacable con informacion alrededor que tiene significado en si mismo, texto que transmiten información completa, como el autor, fecha, objetivo del texto.

#### 2- Nav: Englobara a una lista de enlaces que normalmente será el menú de navegación de la Web. Dentro de Nav se podrá observar una sucesión de etiquetas a o una lista de elementos.

#### 3- Header: Etiqueta de bloque que encerrara a la zona comun de la parte superior de nuestra Web, normalmente estara compuesta por logotipos y demas componentes que se repiten en todas las paginas. No confundir con (head) que lleva solo informacion tecnica para navegadores

#### 4- Footer: Encerrara a la zona comun de la parte inferior de nuestra web, Es posible que nos encontremos el footer dentro de una etiqueta artcle. El footer llevara informacion como derechos de autor, nombre de pagina, contactos. Etc..

#### 5- Section: La etiqueta setion es la etiqueta que hace referencia a un titulo, cuadros de dialogo, cada capitulo de un documento, cada una de las TAB.

#### 6- Main: Es la etiqueta que llevara el contenido principal de nuestra web, seria lo que normalmente va entre la etiqueta (Header y Footer.) Normalmente suele ser hija de la etiqueta (Body)

#### 7- Aside: Seria la contra posicion del (Main) iria todo el contenido de poca relevacion, no principal o contenido secundario. Por ejemplo, banners, zonas de navegacion o eventos (Adelante, atras, sigueinte) tambien se suele colocar dentro de barras lateales Slides, o contenido que no aporta en si información detallada o, autores, objetivo en concreto, se puede utilizar para colocar elementos como redes sociales, contactos, publicidad etc.

## - Etiquetas Semanticas HTML

##### Son etiquetas que nos permiten aportar informacíon precisa a los navegadores, con lo cual podran identificar facilmene nuestro contenido que requerimos mostrar o encontrar, aporta valor y enriquece el codigo, haciendolo mas manejable y adecuado, a nivel visual funciona igul que etiquetas similares que no transmiten o aportan semantica, sin embargo, a nivel tecnico y de navegador o Backend si que aporta buenos resultados.

#### 1- Strong: Aporta mayor relevacion y valor semantico al texto al cual se le asigna, es una etiqueta de linea, con lo cual se aplicara su valor o funcion al texto siguiente de la etiqueta, y lo resaltara en "Negrita", el navegador con esto le dara mayor relevancia con respecto del texto y la mostrara como mas importante.

#### 2- Em: Aporta relevancia alñ texto pero no tanto como strong pero si le asignara el valor semantico, por ejemplo, lo colocara en cursiva para resaltar visualmente ante el resto del texto

#### 3- Time: Es una etiqueta de linea normal, se utilizara para marcar texto con una fecha, hora y tiempo y momento en el cual se accedio al texto o documento. Sirve tambien para webs que no tengan interface visual, y se muestren de forma diferente, nos ayudara a identificar el tipo de documento y etiquetas y hora

#### 4- Timestamp: Lo usaremos para marcar una fecha y hora. Accesibilidad, dispone de un atributo datetime en formato string, que sobre todo se utiliza a nivel de BackEnd en programacion para mostrar, indicar fechas de ocurrencia de eventos y el sistema pueda saber y ademas mostrar los eventos que ocurren en el tiempo

#### 5- Addres: Lo usaremos para indicar la forma de contacto o direccion que mostraremos en nuestra Web. Accesibilidad, Puede ser una URL, una direccion, un email, forma de contactar en caso de no ofrecer una interface visual y poder conectar con algun usuario y  etc.

## - Etiquetas de Agrupación

##### - Sirve para agrupar e identificar una sección específica, para darle un estilo visaul (CSS) y Funcionalidad (Javascript) Por convecion es mejor tener mas etiquetas de agrupación sin "Excederse" que te falten debido a posteriormente puedas requerir agregar funcionalidad y valor a la Web y no las tengas disponibles. Seria más complicado el UpGrade de la pagina.

#### 1- Etiqueta Div:  Es ua etiqueta de bloque y agrupación. Contiene todos los atributos de evento, sirve para agrupar una o varias etiquetas. Con titulo por ejemplo H2, y a su vez tiene internamente otros o varios "Div" de noticias o conceptos, sin embargo a nivel semantico es mejor utilizar la etiqueta "Article" o incluso utiizar una etiqueta "Section"

#### 2- Etiqueta Spam: Es una etiqueta de linea, que puede contener más etiquetas de linea, NO ASI ETIQUETAS DE BLOQUES.  Limita a los navegadores y obstaculiza la funcion del navegador si empleamos o queremos incluir una etiqueta de bloque dentro de un etiqueta de linea. Se puede usar como etiqueta Div, por ejemplo, dado un conjunto de texto agregarla algun tipo de funcionalidad, estilo al texto seleccionado, no cambia el flujo normal del texto.

#### 3- Etiqueta Blackquote: Se utiliza para indicar que el texto pertenece a otro sitio externo del cual se indica la fuente, es una etiqueta de bloque, atributos comunes y eventos, atributos especificos "Cite" de tipo URL para indicar el origen de la "Cita".

#### 4- Etiqueta Hr: Normalmente se conoce como etiqueta divisora o separación semantica, permite separa un conjunto de información de otra diferente, de distinto significado u objetivo. Es una etiqueta semantica. Visualmente el navegador pinta una linea divisoria al final o inicio de linea de codigo.

#### 5- Figure y Figcaption: Son etiquetas de agrupación para imagenes, encerrará a una etiqueta "img" básica. Se manejará mucho mejor con CSS en el futuro. Esta etiqeuta puede contener no solo imagenes si no que tambien videos, o elementos multimedios. La etiqeuta figcaption contendra la informacion tecnica de la etiqueta, y tambien contendra la informacion del elemento que se encuentra dentro de la etiqueta "Figure" la informacion aparecera tipo un pie de página. Ambas etiqeutas son necesarias y se complementan una de otra, no se debe utilizar por separadas.

## - Etiquetas de Listas y Listas anidadas

#### - Etiquetas "ul", "ol" son etiquetas que definen listas ordenadas o desordenadas, ul y ol son etiquetas de bloque, que forman bloques de información reprsentado en listas ordenadas (ol) que poseen un orden o jerarquia, tambien hay listas no ordenadas (ul) que serian listas random que no es necesario ordenar, dependiendo el caso que se utiliza. La etiqueta ( ul ) ofrece un poco de padding o margen a la lista.

#### - Etiquetas Li: Son etiquetas que dependen de etiquetas padre como (ol y ul) y se comportaran de acuerdo a la lista padre que las contenga. Las etiquetas "Li" son etiquetas que permiten anidar otras listas, teniendo en cuenta que esas listas siempre seran con etiquetas de listas (ul, ol y li) Siempre deben tener en cuenta que las etiquetas "li" deben cerrarse siempre como el resto de las etiquetas pero estas con mayor cuidado.

#### - Etiquetas dl: Son lista de descripcion de elementos, o describirlos, sobre todo utilizadas en diccionarios o textos indices. Las etiquetas hijas de "dl" son las etiquetas dt y dd, la estiqueta "dt": Sugiere el termino a definir y la etiqueta "dd": Definición de termino.

## - Etiquetas no recomendadas Actualmente

#### 1- Etiqueta b: Funciona o sirve para colocar el texto en "Negrita" pero sin valor semantico, y aunque tiene una retrocompatibilidad alta, no se aconseja el uso. Es similar al uso de "Strong" que si tiene valor semantica.

#### 2- Etiqueta i: Sirve para coloca el texto en cursiva o "Italics", sin envargo para eso tenemos la etiqueta (em) que si tiene valor semantico.

#### 3- Etiqueta Small o u: Sirve para colocar las letras con menor tamaño pero carecen de semantica.

## - Herramientas para Trabajar en Webs

#### 1- Increible ChatGPT: Es una extension para Google. Captura de pantalla y graficos, hace una imagén de toda la Web tipo OCR en FireFox es nativo.

#### 2- Can I Include: Es una Web que te puede ofrecer infomración sobre cuales etiquetas HTML puedes utilizar dentro de otra. o pueda contener otra etiqueta.

#### 3-



Enlace de donde se encuentra el mapa libre real: [opencellid.org/#zoom=16&amp;lat=37.77889&amp;lon=-122.41942](https://opencellid.org/#zoom=16&lat=37.77889&lon=-122.41942)

[Enlace que me envia Opencellid para conectarme en log_web: ](https://my.opencellid.org/dashboard)[my.opencellid.org/dashboard/magicauth?l=db0ccc08d15408ac041dbafd450f381a2df37faa&amp;e=dmlrdG9yZW1pbGV0aWNAZ21haWwuY29t&amp;ref=opencellid](https://my.opencellid.org/dashboard/magicauth?l=db0ccc08d15408ac041dbafd450f381a2df37faa&e=dmlrdG9yZW1pbGV0aWNAZ21haWwuY29t&ref=opencellid)

Correo electrónico: viktoremiletic@gmail.com

Clave de acceso Opencellid: Z2naGTk47ZXk!4B

Token: pk.35df342da9695f19345f7d6d8d9e4eed

Solo 5 solicitud disponibles version Free:


Error que muestra la Web cuando hago click el enlace de Opencellid de nuestro Grid dentro de la seccion Torres/Antenas.

# 403 Forbidden

---

nginx/1.24.0
