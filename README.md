# Biblioteca Electrónica Textual del Teatro en Español de 1868-1936 (BETTE)

## Introducción
La *Biblioteca Electrónica Textual del Teatro en Español* (BETTE) es una colección de textos teatrales de la Edad de Plata española, codificada en XML-TEI por el grupo GHEDI de la Universidad Internacional de la Rioja (UNIR). En esta primera fase (BETTE 1.0) hemos publicado 24 textos de 8 autores (Lorca, Valle, Munoz, Echegaray, Unamuno, Valera, Clarin y Dicenta).

## Estado del Arte y Motivación
El teatro hispánico ha sido objeto de numerosos e importantes proyectos dentro de las Humanidades Digitales en nuestra lengua. Proyectos como (solo por citamos algunos de los más importantes) *TESO* (Simón Palmer 1997), *Biblioteca Digital Arte Lope* (Oleza Simó 2013), o *Canon 60* (Oleza Simó 2014) ya han trabajado en XML-TEI codificando obras de teatro en español. Sin embargo hasta ahora se ha trabajado prácticamente en exclusiva el período áureo de este género literario, dejando de lado otras épocas. Además, los citados proyectos no ponen a disposición de la comunidad investigadora los datos XML-TEI originales, sino apenas una exportación en HTML.

Por otro lado, en la actualidad numerosos grupos están trabajando en diferentes áreas de la Edad de Plata: revistas por *Revistas Culturales 2.0* (Ehrlicher und Rissler-Pipka 2015), novelas por *Corpus of Spanish Novel from 1880-1940* (Calvo Tello 2015), metadatos por *Mnemosine* () o poesía por *DISCO* (Ruiz 2017).

Como observamos, hay notable actividad en las Humanidades Digitales tanto en el teatro como en la Edad de Plata, pero percibíamos una laguna en la intersección de ambas, que ahora el grupo GHEDI y el proyecto BETTE cubren.

Esta laguna podría estar en parte motivada por la situación legal que muchos autores de esta época tienen. Sin embargo en 2017 algunos de los más importantes autores de la literatura española pasaron a dominio público: Lorca, Valle, Unamuno o Muñoz Molina. El grupo GHEDI y BETTE ponen a disposición de la comunidad investigadora los textos de estos autores en el lenguaje de marcado estándar en las Humanidades Digitales: XML-TEI.

## Corpus
Como ya se ha señalado, el corpus actualmente dispone de 24 textos de 8 autores diferentes, con la siguiente distribución:

* Lorca	5
* Valle	5
* Munoz	4
* Echegaray	2
* Valera	2
* Unamuno	2
* Clarin	1
* Dicenta	1

La selección de autores y de textos ha seguido varios criterios, principalmente:

1. La existencia de alguna digitalización del texto (en formatos HTML, ePUB, PDF...)
2. La canonización del autor y del texto
3. Los intereses de los investigadores del grupo
4. Conseguir diferenes textos del mismo autor, sin que ningún autor tenga un peso desproporcionado en el corpus total

Somos conscientes de que criterios estrictamente filológicos serían deseables, pero también de que conseguir aplicarlos conlleva una mayor cantidad de tiempo y de medios, que hasta ahora no hemos tenido a disposición. Confiamos que en el futuro el corpus pueda ampliarse, así como conseguir un mejor equilibrio entre diferentes criterios (época, subgénero, autor).

## Codificación

Los textos están codificados en XML-TEI P5 y validados con un esquema de un subconjunto de elementos y atributos a partir de *TEI all*. Dentro de la estructura textual, los siguientes elementos han sido marcados de manera específica:

* acotaciones
* nombre de personajes
* lista de personajes
* referencias a nombres de personajes (mediante nombre propio) dentro del texto
* cursiva
* encabezamientos
* paratextos iniciales y finales

Cada uno de los personajes del texto ha recibido un identificador que es utilizado en cualquier mención (lista de personajes, como personaje que habla, como referencia en acotaciones o texto literario). En casos complejos (agrupaciones espontáneas de personajes, personajes colectivos, personajes que no aparecen en la lista de personajes, cambios de nombres de personajes) hemos priorizado la identificación sistemática de cada uno de los personajes de manera individual.

Además, las diferentes secciones del texto (*div*'s) están caracterizadas mediantes atributos *type* que señalan si son actos o escenas. Este elemento también está caracterizado mediante un número que corresponde a su encabezamiento o (en caso de no haberlo) al orden dentro de la obra. De esta manera el investigador puede seleccionar si quiere trabajar con escenas o actos, y no sencillamente mediante divisiones de cierto grado.

Algunas de las obras han sido cotejadas filológicamente con una obra de referencia (de poder ser, con la primera edición). Se puede saber si la obra ha sido cotejada si encontramos un elemento *change* con el atributo y valor: *status="compared"*. Somos conscientes de que la cotejación filológica es importante, y por eso comenzamos a realizarlo. Sin embargo el grupo se decidió por trabajar con grafos y redes sociales de personajes. Dentro de este tipo de estudios (con un enorme crecimiento internacional actualmente), el texto es en la mayoría de los casos ignorado, utilizándose exclusivamente la estructura de coapariciones de personajes en secciones de la obra. En el mejor de los casos, el texto es reducido enormemente a la cantidad de caracteres o palabras que un personaje dice cada vez. Es decir, la mayoría de la información cualitativa que un cotejo filológico traería, serían ignoradas por este tipo de análisis. Por eso decidimos priorizar otros aspectos del trabajo y postergar el cotejo filológico para pasos futuros.

## Metadatos
En el *TEIheader* se encuentran los principales metadatos sobre el texto y el autor, ambos señalados mediantes identificadores VIAF y de la Biblioteca Nacional de España. También se ha puesto empeño en identificar de manera explícita los diferentes estadios de una obra hasta llegar a este punto. En concreto citamos cuatro posibles estadios:

* estreno
* primera publicación
* edición digital utilizada
* edición utilizada para su cotejo

Además, cada obra contiene un resumen especificando qué ocurre en cada acto. De esta manera se facilita a los investigadores un primer acercamiento en un par de párrafos a la obra, información que puede utilizarse como el puente entre el *close reading* de saber qué ocurre en el texto, y el *distant reading* de herramientas digitales.

## Aplicacione en Investigación

Como ya se ha señalado, el grupo está actualmente explorando estas obras mediante representaciones de redes sociales de los personajes en forma de grafo. Esta es un área de gran desarrollo en las Humanidades Digitales internacionales actualmente, con trabajos punteros de investigadores como Moretti, Craig, Jannidis, Schöch, Mark (?), Fischer (...), Rochat o Grandjen.

EL objetivo de esta área de las HD es recoger el modelo teórico desarrollado desde las matemáticas y utilizado en diferentes áreas (física, biología, sociología), y aplicarlo a la literatura, en concreto a la interacción entre personajes del texto.

Siguiendo la propuesta de Marcus (1973), popularizada por Moretti (2005), las obras (principalmente de teatro, aunque no solo), podrían considerarse como una red de personajes. Esos personajes estarían conectados mediante aristas en caso de que hablen entre sí (o, de manera simplificada, en caso de que aparezcan en la misma escena). Este modelo permite no solo visualizar estas redes de personajes, sino que también pone a disposición del investigador un conjunto de conceptos y metodologías que permiten analizar el objeto (en este caso, obras teatrales) de manera innovadora y reproducible.

## Futuros pasos

En la actualidad el grupo se encuentra trabajando en una segunda versión del corpus. Esta versión pondrá el foco en detallar numerosa información de cada uno de los personajes: sexo, papel dentro de la obra, tipo de personaje, etcétera. El objetivo es poder utilizar esta información para evaluar los grafos. La siguiente versión además contendrá más metadatados en diferentes áreas, como una mejor versionización de los textos, subgénero literario, etcétera.

## Equipo
Esta fase del proyecto ha sido liderada por Concepción María Jiménez. Teresa Santa María Fernández fue la responsable de la dirección del cotejo filológico y José Calvo Tello fue responsable de la parte técnica. El corpus ha sido creado gracias al trabajo del equipo completo (en orden alfabético):

* José Calvo Tello
* Guadalupe Frutos
* Mireya Fernández
* Sila Gómez
* María López Aboal
* Concepción María Jiménez
* Beatriz Martínez Nieto 
* Elenar Martínez Carro
* Marta Ortiz
* Julio Peiro
* María García Sánchez
* Teresa Santamaría
* María Simón Parra
* María Ángeles Somalo


## Cómo citar BETTE

Para citar la colección como tal:
* María Jiménez, Concepción, y Santa María Fernández, Teresa:  *Biblioteca Electrónica Textual del Teatro en Español* (BETTE), La Rioja, Unir: 2017. \<\>

Para citar la presentación del corpus en su versión 1.0:
* María Jiménez, Concepción, Martínez Carro, Elena, Santa María Fernández, Teresa, Calvo Tello, José, Simón Parra, María, Martínez Nieto, Roxana Beatriz, García Sánchez, María, *BETTE: Biblioteca Electrónica Textual del Teatro en Español de la Edad de Plata*, Málaga, Congreso HDH: 2017 \<\>

Para citar un artículo sobre la planificacioń de BETTE:
* Gómez, Sila, Calvo Tello, José, González, Juana María y Vilches, Rocío. 2015. ‘Hacia Una Biblioteca Electrónica Textual Del Teatro En Español de 1868-1936 (BETTE).’ Texto Digital 11 (2): 171–84. \<https://periodicos.ufsc.br/index.php/textodigital/article/view/1807-9288.2015v11n2p171/30960\>


## Referencias

* Calvo Tello, José. 2015. *Corpus of Spanish Novel from 1880-1940*. Sp. Würzburg: University of Würzburg. https://github.com/cligs/textbox/tree/master/es/novela-espanola.
* Ehrlicher, Hanno, and Nanete Rißler-Pipka. 2015. *Revistas Culturales 2.0* . Augsburg: Universität Augsburg. https://www.revistas-culturales.de/es.
* Oleza Simó, Joan. 2013. *Biblioteca Digital Arte Lope*. Valencia: Universitat de València. artelope.uv.es/biblioteca.
* ———. 2014. *Canon 60*. Valencia: Universitat de València. http://tc12.uv.es/index.php/produccion-cientifica/edicion-del-patrimonio-teatral/canon-60.
* Ruiz, Pablo, Clara Martínez Cantón, and José Calvo Tello. 2017. *DISCO*.
* Simón Palmer, María del Carmen. 1997. *Teatro Español Del Siglo de Oro*. Ann Arbor: ProQuest. teso.chadwyck.com.



