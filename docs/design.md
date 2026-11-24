Modelo de datos:
Libro:
Campo       |   Tipo    |    Obligatorio    |     Restricciones
id              GUID         Si                   Unico
titulo          Texto        Si                   No vacío
cantudadPaginas Entero       Si                   Mayor a 0
editorial       Texto        Si                   No vacío
isbn            Texto        Si                   Formato válido
costoUsd        Decimal      Si                   Mayor o igual a 0

Diseño de API:

Operación   |   Método  |   Exito   |   Errores
Listar          GET         200         n/a
Buscar          GET         200         n/a
Obtener uno     GET         200         404
Crear           POST        201         400, 409 (id duplicado)
Modificar       PUT         200         400, 404, 409 (nuevo id ya existe)
Eliminar        DELETE      204         404



