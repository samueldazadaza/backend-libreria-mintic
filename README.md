"# api-books"

##### Intrucciones para correr y utilizar la api en local:

---

se crea una base de datos en mysql llamada 👉 springboot

y se ejecuta en la raiz del proyecto la sigiente linea

mvnw.cmd spring-boot:run

##### para utilizar la api books

---

para crear libro ejecuta en postman en POST a la url: http://localhost:8080/books
{
"titulo": "codigo da vinci",
"autor": "dan brown",
"genero": "novela",
"fecha_publicacion": "1999-11-10",
"editorial": "anonima",
"cantidad": 77,
"precio": 100000
}

para modificar libro (agregas id a modificar) ejecuta en postman en POST a la url: http://localhost:8080/books
{
"id_libro":4
"titulo": "codigo da vinci",
"autor": "dan brown",
"genero": "novela",
"fecha_publicacion": "12-11-1999",
"editorial": "anonima",
"cantidad": 77,
"precio": 100000
}

para eliminar un libro, digita el id en la POSTMAN con el metodo DELETE, ejemplo: http://localhost:8080/books/1

los datos de los libros quedan en: http://localhost:8080/books

para ver un libro en especifico con el id: http://localhost:8080/books/2

para ver lista de libros por generos: http://localhost:8080/books/query?genero=ficcion

