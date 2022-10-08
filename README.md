
"# api-books"

##### Intrucciones para correr y utilizar la api en local:

---

se crea una base de datos en mysql llamada 👉 springboot

y se ejecuta en la raiz del proyecto la sigiente linea

mvnw.cmd spring-boot:run

##### para utilizar la api books

---

CREATE /// para crear libro ejecuta en postman en POST a la url: http://localhost:8080/books
{
"titulo": "2 ///////// Años de Soledad22",
"autor": "Gabriel García Márquez",
"genero": "Realismo Mágico",
"fecha_publicacion": "1967-06-05",
"editorial": "Sudamericana de Buenos Aires",
"cantidad": 12,
"precio": 50000
}

READ /// para LEER libros ejecuta en postman en GET a la url: http://localhost:8080/books
//arrojara un array con los libros en base de datos mysql

UPDATE /// para modificar libro (agregas id a modificar en el endpoint) ejecuta en postman en POST a la url: http://localhost:8080/books
{
"id_libro": 3,
"titulo": "2 ///////// Años de Soledad22",
"autor": "Gabriel García Márquez",
"genero": "Realismo Mágico",
"fecha_publicacion": "1967-06-05",
"editorial": "Sudamericana de Buenos Aires",
"cantidad": 12,
"precio": 50000
}

DELETE /// para eliminar un libro, digita el id en la POSTMAN con el metodo DELETE, ejemplo: http://localhost:8080/books/1
//DIGITA EN EL ENDPOINT EL ID DEL LIBRO

para ver un libro en especifico con el id: http://localhost:8080/books/2

para ver lista de libros por generos: http://localhost:8080/books/query?genero=ficcion

---

configuracion local anterior:

spring.datasource.url=jdbc:mysql://127.0.0.1:3306/springboot
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto = update

---

configuracion remota:

# port

server.port=${PORT:8080}

spring.datasource.url = jdbc:mysql://db4free.net:3306/stocklibreria
spring.datasource.username = grupo09
spring.datasource.password = Grupo092022\*
spring.jpa.hibernate.ddl-auto = update

---

importar cors para acceso desde navegador:

@RestController
@CrossOrigin(origins = "\*")
@RequestMapping("/libros")
public class LibrosController {


    --------------------
para correr en local es necesario correr XAMPP y activar APACHE y MYSQL
👇👇👇// EL SERVIDOR QUEDARA ACTIVO EN LA URL👇
http://localhost:8080/books/