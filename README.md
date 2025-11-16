# Menú Dinámico con JSON

Este proyecto implementa un **menú dinámico** generado a partir de una estructura de datos externa (JSON), permitiendo agregar, editar y eliminar opciones sin modificar el código fuente.

## Características principales

* Menú completamente dinámico basado en un archivo **menu.json**.
* Soporte para **iconos**, **submenús** y estructura anidada.
* Sistema de edición mediante formulario:

  * Agregar nuevas opciones.
  * Validaciones de campos.
  * IDs únicos.
* Actualización del menú **sin recargar la página**.
* Persistencia con **localStorage**.
* Diseño **responsive** para móviles, tablets y escritorio.


## Estructura JSON utilizada

```json
{
  "menu": [
    {
      "id": 1,
      "nombre": "Inicio",
      "enlace": "/inicio",
      "icono": "home"
    },
    {
      "id": 2,
      "nombre": "Servicios",
      "enlace": "/servicios",
      "icono": "settings",
      "submenu": [
        { "id": 21, "nombre": "Consultoría", "enlace": "/consultoria" },
        { "id": 22, "nombre": "Desarrollo", "enlace": "/desarrollo" }
      ]
    }
  ]
}
```

## Tecnologías utilizadas

* **React** (Frontend dinámico)
* **JavaScript**
* **CSS** (Responsive)
* **JSON** (Estructura de datos)


## Cómo funciona

1. La aplicación carga los datos desde **menu.json** ubicado en `public/`.
2. El componente `Menu` renderiza dinámicamente cada opción del menú.
3. El usuario puede agregar nuevas opciones a través del formulario de `MenuEditor`.
4. Los cambios se guardan en **localStorage**, permitiendo persistencia sin backend.
5. El menú se actualiza automáticamente sin recargar toda la página.


## Instalación y uso

1. Clona el proyecto:
   git clone https://github.com/usuario/proyecto-menu
   
2. Instala dependencias:
   npm install
  
3. Ejecuta el servidor de desarrollo:
   npm run dev

4. Abre en el navegador:
http://localhost:5173

## Validaciones incluidas

* Identificadores (**ID**) únicos.
* Los enlaces deben comenzar con **/**.
* Evita agregar opciones vacías.
* Sanitización básica para prevenir entradas inseguras.

## Responsividad

El menú adapta automáticamente su estructura en tamaños:

* Móvil
* Tablet
* Escritorio

Incluye estilos que modifican la dirección del menú y comportamiento del submenu.

## Qué se aprendió en este proyecto

* Crear componentes reactivos basados en datos externos.
* Actualizar interfaces dinámicamente sin recargas.
* Manejar persistencia con `localStorage`.
* Validaciones y estructura de menús complejos.
* Construcción de UI responsiva.

## Futuras mejoras

* Editor visual de submenús.
* Integración con backend (API).
* Panel de administración protegido.

## Autor

**Pascual Pimentel Vicente**

Proyecto desarrollado como ejercicio práctico para construir un menú dinámico editable sin modificar código fuente.

