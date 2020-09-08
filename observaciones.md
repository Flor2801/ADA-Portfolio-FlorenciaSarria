### Comentarios Generales

Flor, en primer lugar tengo que felicitarte por un un excelente trabajo. Seguiste a la perfección los requisitos pedidos a nivel diseño y estructura, y aún así lograste con detalles muy bien pensados que tu portfolio se sienta original y tuyo. Me encanta la paleta de colores, la elección de iconos e imagenes, todo hace un efecto muy amigable y el resultado es un portfolio atractivo, digno de una profesional. Si bien no puedo evaluar el aspecto visual, ya que no es parte del programa ni una habilidad requerida para una desarrolladora front end, sí quiero comentar lo linda que se ve tu web. 

El responsive en particular te quedó perfecto, no hay resolución en donde tu web no se vea a la perfección. Esa atención al detalle es muy valiosa. Se nota mucho que en este trabajo hay tiempo, ganas y aprendizaje invertido - que te esforzaste en aplicar lo aprendido y aprender más aún durante su desarrollo. Espero que estés muy orgullosa de vos misma; yo, sin dudas, lo estoy. 

Tu repositorio está ordenado, y cuenta con un buen README. Debo mencionar que hay relativamente pocos commits: una vez que hiciste la estructura base, ahi si fuiste muy prolija agregandolos de a poco, pero hubira estado bueno ver la evolucion desde el comienzo. Si bien entiendo que no es fácil subir un código cuando está recién empezado y lleno de problemas, es lo mejor, tanto para irse acostumbrando una a hacerlo, como para permitir que colegas (y profes!) puedan ver la evolución del código y encontrar rapidamente los commits en donde se hicieron determinados cambios. Cuando trabajamos en equipo es muy importante hacer commits breves, asi cualquier cambio puede identificarse facilmente. 

Si bien tu HTML esta muy bien indentado, dejas muchisimos saltos de linea entre secciones o estilos sin una intencion determinada, que dificultan bastante la lectura de tu codigo. Quiza valga la pena que busques algun linter (hay un monton en las extensiones de visual studio, yo uso Prettier) para que te formatee las cosas al guardar, o que te acostumbres al clic derecho + format document de VSCode (aunque toma en cuenta que no funciona para CSS, ahi vas a tener que bajarte alguna extension).

Tu CSS esta muy prolijo, francamente a un nivel mucho mayor de lo que esperamos de alguien con tu experiencia, pero el tabulado no esta bien. Dentro de una media query, siempre dejamos tabulado de dos o 4 espacios, justamente para indicar que estamos dentro de una. En tu caso no haces esto, y se dificulta mucho saber si estamos en una media query o en los estilos generales. Tu primera media query, ademas, nunca se cierra. No te trae problemas - en este caso - pero podria haber sido desastroso, porque es un error dificil de encontrar. Por otro lado, veo que el estilo en las media queries muchas veces es innecesario - son mucho mas largas de lo que deberia ser necesario. 

En ese mismo sentido, algo que me llama la atencion es que en las media queries repetis *todos* los estilos de algunos elementos. Esto no es necesario. Si en desktop pusimos que la tipografia es Montserrat, no hace falta ponerlo de nuevo en la media query. **Solo ponemos los estilos que queremos cambiar.** Esto es importantisimo, es algo que se te evaluara en ofertas laborales y que tenes que tener en claro al momento de superar esta etapa. Por ejemplo, el elemento "hola" en desktop esta asi:

```css
.hola {
   width: 100%;
   height: 100%;
   display: flex;
   justify-content: space-around;
   align-items: center;
   padding-bottom: 30px;
   padding-top: 30px;
   
}
```

Y en la media query de 850px, asi: 

```css
.hola {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-bottom: 30px;
 }
```

El unico cambio es que ya no esta el padding top, pero, atencion! El padding top se sigue aplicando aunque no este en la media query, porque los estilos que no se contradicen explicitamente se heredan de desktop a las media queries. Por lo tanto haber agregado este elemento .hola en la media query fue totalmente inutil: no afecta en nada. Como este, hay muchisimos mas - la mayoria. 

Usas muchisimas veces width: 100% y height: 100%, una orden que no deberia ser necesaria (ni lo es en tu codigo) salvo en elementos especificos como imagenes. Los elementos en bloque ya tienen de por si un width de 100%. Tambien agregas muchas cosas innecesarias como "flex-direction: row" (que se pone por defecto). Abundan tanto en tu CSS que no pude marcarlas a todas. Proba bien si una orden de css es necesaria luego de escribirla: no es bueno tener CSS innecesario ya que complica mucho el mantenimiento del codigo. 


Sé que puedo ser un poco quisquillosa en las correcciones. No es la intención que sientas que hiciste un mal trabajo, porque no es así: tu trabajo es fantástico. Mi tarea es comentarte todo lo que vea para que sea más fantástico aún. 


### Nota final: 9

Nota desagregada: 
✅ Estructura correcta de documento HTML.
✅ Respeta la consigna 
✅ Respeta el diseño dado 
✅ Responsive funciona correctamente
✔️ Código bien indentado --> con observaciones
✅ Comentarios que permiten mejorar la legibilidad del código.
✅ Uso correcto de etiquetas semánticas.
✅ Buenos nombres de clases
✅ Reutilización de estilos.
❌ Código CSS ordenado.
✅ Commits con mensajes adecuados.

