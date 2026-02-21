# Enunciado: Diseño, Implementación y Documentación de una API CRUD Profesional

[# api-floreria](https://6987730d8bacd1d773ed622b.mockapi.io/Producto

Proyecto: API de Floristeria
Estudiantes: Paola Andrea Arimendy Cardeño
             Mayerlin Cubides 
             Johana Peña Henao

URL de la API: https://6987730d8bacd1d773ed622b.mockapi.io/Producto

# 1.Modelo de Datos Diseñado

Se congifuró el recurso Flores con la siguiente estructura de datos:

{
    "Nombre": "Rosa",
    "Descripcion": "Aromatica - Simbolo del amor",
    "Detalles": {
      "Colores": "Rojo, Rosa, Blanco, Amarillo",
      "Tamaño": "5 a 12 cm"
    },
    "Usos": [
      "Ramos",
      "Decoracion"
    ],
    "Disponible": false,
    "id": "1"
  }

  # 2.Bitácora de Operaciones CRUD (Respuestas de Postman)

  **A.Obtener todos los registros (GET)**

  Status Code: 200 OK 
  Respuesta de Postman: 

  [
    {
        "Nombre": "Rosa",
        "Descripcion": "Aromatica - Simbolo del amor",
        "Detalles": {
            "Colores": "Rojo, Rosa, Blanco, Amarillo",
            "Tamaño": "5 a 12 cm"
        },
        "Usos": [
            "Ramos",
            "Decoracion"
        ],
        "Disponible": false,
        "id": "1"
    },
    {
        "Nombre": "Tulipan",
        "Descripcion": "Pétalos en forma de copa",
        "Detalles": {
            "Colores": "Rojo, Amarillo, Purpura, Blanco",
            "Tamaño": "6 a 10 cm"
        },
        "Usos": [
            "Ornamental",
            "Arreglos florales"
        ],
        "Disponible": true,
        "id": "2"
    },
    {
        "Nombre": "Girasol",
        "Descripcion": "Grande, sigue la luz solar",
        "Detalles": {
            "Colores": "Amarillo con centro marrón",
            "Tamaño": "20 a 30 cm"
        },
        "Usos": [
            "Decoración",
            "Semillas comestibles"
        ],
        "Disponible": false,
        "id": "3"
    },
    {
        "Nombre": "Orquideas",
        "Descripcion": "Exótica y Elegante",
        "Detalles": {
            "Colores": "Blanco, Purpura, Rosa, Amarillo",
            "Tamaño": "3 a 15 cm"
        },
        "Usos": [
            "Ornamentación e interiores",
            "Regalos"
        ],
        "Disponible": true,
        "id": "4"
    },
    {
        "Nombre": "Lirio",
        "Descripcion": "Fragancia Intensa",
        "Detalles": {
            "Color": "Blanco, Naranja, Rosa, Purpura",
            "Tamaño": "10 a 20 com"
        },
        "Usos": [
            "Ramos de bodas",
            "Jardines"
        ],
        "Disponible": false,
        "id": "5"
    },
    {
        "Nombre": "Margarita",
        "Descripcion": "Sencilla y Alegre",
        "Detalles": {
            "Colores": "Blanco, Amarillo, Rosa, Rojo, Azul, Naranja",
            "Tamaño": "2 a 5 cm"
        },
        "Usos": [
            "Decoración campestre",
            "Ramos"
        ],
        "Disponible": false,
        "id": "6"
    }
]

 **B.Creación de un nuevo registro (POST)**

  Status Code: 201 Created
  Cuerpo enviado en Postman:

   {
        "Nombre": "Dalia",
        "Descripcion": "Versatil y Llamativa",
        "Detalles": {
            "Colores": "Blanco, Amarillo, Rojo, Rosado",
            "Tamaño": " 20 a 25 cm"
        },
        "Usos": [
            "Ornamental",
            "Gastronomica"
        ],
        "Disponible": false

    }

Respuesta de Postman:

{
    "Nombre": "Dalia",
    "Descripcion": "Versatil y Llamativa",
    "Detalles": {
        "Colores": "Blanco, Amarillo, Rojo, Rosado",
        "Tamaño": " 20 a 25 cm"
    },
    "Usos": [
        "Ornamental",
        "Gastronomica"
    ],
    "Disponible": false,
    "id": "8"
}

 **C.Consultar un registro individual (GET)**

Endpoint: https://6987730d8bacd1d773ed622b.mockapi.io/Producto/2
Status Code: 200 OK

Respuesta De Postman:

{
    "Nombre": "Tulipan",
    "Descripcion": "Pétalos en forma de copa",
    "Detalles": {
        "Colores": "Rojo, Amarillo, Purpura, Blanco",
        "Tamaño": "6 a 10 cm"
    },
    "Usos": [
        "Ornamental",
        "Arreglos florales"
    ],
    "Disponible": true,
    "id": "2"
}

**D. Actualización de un registro (PUT):**

Status Code: 200 OK
Modificación: se actualiza el uso y el color



{
    "Nombre": "Tulipan",
    "Descripcion": "Pétalos en forma de copa",
    "Detalles": {
        "Colores": "Rojo, Amarillo, Purpura, Blanco",
        "Tamaño": "6 a 10 cm"
    },
    "Usos": [
        "Ornamental",
        "Arreglos florales"
    ],
    "Disponible": true,
    "id": "2"
}

Respuesta Postman:


{
    "Nombre": "Tulipan",
    "Descripcion": "Pétalos en forma de copa",
    "Detalles": {
        "Colores": "Rojo, Amarillo, Azul, Blanco",
        "Tamaño": "6 a 10 cm"
    },
    "Usos": [
        "Regalo",
        "Arreglos florales"
    ],
    "Disponible": true,
    "id": "2"
}

**E. Eliminación de un registro (DELETE)**

Status Code: 200 OK

Respuesta de Postman:

{
    "Nombre": "Girasol",
    "Descripcion": "Grande, sigue la luz solar",
    "Detalles": {
        "Colores": "Amarillo con centro marrón",
        "Tamaño": "20 a 30 cm"
    },
    "Usos": [
        "Decoración",
        "Semillas comestibles"
    ],
    "Disponible": false,
    "id": "3"
}

**F. Validación de recurso inexistente (GET 404)**

Status Code: 404 NOT FOUND

Respuesta Postman

"Not found"


**3. Resumen de Endpoints y Códigos HTTP**

- **Base URL:** https://6987730d8bacd1d773ed622b.mockapi.io

| Endpoint | Método | Descripción | Códigos HTTP esperados |
| --- | --- | --- | --- |
| /Producto | GET | Obtener todos los productos (flores) | 200 OK |
| /Producto | POST | Crear un nuevo producto | 201 Created |
| /Producto/{id} | GET | Obtener un producto por su ID | 200 OK / 404 Not Found |
| /Producto/{id} | PUT | Actualizar un producto por su ID | 200 OK / 404 Not Found |
| /Producto/{id} | DELETE | Eliminar un producto por su ID | 200 OK |

Puedes usar la **Base URL** junto con los endpoints relativos mostrados arriba. Los códigos indicados son los más comunes para cada operación; en errores se pueden devolver códigos como `400`, `401` o `500` según el caso.)
