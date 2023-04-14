# Laboratorio 5
### Juan Pablo Poveda Cañon
### Gonzalo Pedro Falco

#### PARTE II
1. Revise la clase SampleServlet incluida a continuacion, e identifique qué hace
2. En el pom.xml, modifique la propiedad "packaging" con el valor "war". Agregue la siguiente dependencia
3. Revise en el pom.xml para qué puerto TCP/IP está configurado el servidor embebido de Tomcat (ver sección de plugins).
4. Compile y ejecute la aplicación en el servidor embebido Tomcat, a través de Maven con:
 * mvn package
 * mvn tomcat7:run
5. Abra un navegador, y en la barra de direcciones ponga la URL con la cualse le enviarán peticiones al ‘SampleServlet’. Tenga en cuenta que la URL tendrá
como host ‘localhost’,como puerto, elconfigurado en el pom.xml y el path debe ser el del Servlet. Debería obtener un mensaje de saludo.

![imagen 1](https://github.com/gonzafalco7/Laboratorio5/blob/main/post%20diferencia.png)

6. Observe que el Servlet ‘SampleServlet’ acepta peticiones GET, y opcionalmente, lee el parámetro ‘name’. Ingrese la misma URL, pero ahora agregando
un parámetro GET (si no sabe como hacerlo, revise la documentación en http://www.w3schools.com/tags/ref_httpmethods.asp).

![imagen 1](https://github.com/gonzafalco7/Laboratorio5/blob/main/servlet_funcionando_bien.png)

8. En el navegador revise la dirección https://jsonplaceholder.typicode.com/todos/1. Intente cambiando diferentes números al final del path de la url.

![imagen 8](https://github.com/gonzafalco7/Laboratorio5/blob/main/imagen%206.png)

9. Basado en la respuesta que le da elservicio del punto anterior,cree la clase edu.eci.cvds.servlet.model.Todo con un constructor vacío y
los métodos getter y setter para las propiedades de los"To Dos" que se encuentran en la url indicada.

10. Utilice la siguiente clase para consumir el servicio que se encuentra en la dirección url del punto anterior.
11. Cree una clase que herede de la clase HttpServlet (similar a SampleServlet), y para la misma sobrescriba el método heredado doGet. Incluya la anotación @Override para verificar –en tiempo de compilación- que efectivamente se esté sobreescribiendo un método de las superclases.
12. Para indicar en qué URL el servlet interceptará las peticiones GET, agregue al método la anotación @WebServlet, y en dicha anotación, defina la propiedad urlPatterns, indicando la URL (que usted defina) a la cual se asociará el servlet.

![imagen 12](https://github.com/gonzafalco7/Laboratorio5/blob/main/imagen%206.png)

13. Teniendo en cuenta las siguientes métodos disponibles en los objetos ServletRequest y ServletResponse recibidos por el método doGet.

14. Una vez hecho esto, verifique el funcionamiento de la aplicación, recompile y ejecute la aplicación.

![imagen 14](https://github.com/gonzafalco7/Laboratorio5/blob/main/servlet_funcionando_bien.png)

15. Intente hacer diferentes consultas desde un navegador Web para probar las diferentes funcionalidades

![imagen 15](https://github.com/gonzafalco7/Laboratorio5/blob/main/Screenshot%202023-03-17%20145929.png)

* Pruebas donde debería responder con error:

![imagen 15](https://github.com/gonzafalco7/Laboratorio5/blob/main/filenotfound.png)

#### PARTE III

16. En su servlet,sobreescriba el método doPost, y haga la misma implementación del doGet.
