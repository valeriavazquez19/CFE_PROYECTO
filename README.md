**Estructura del Proyecto con Diseño Responsivo**

### 1. Organización de Archivos
El proyecto está organizado en varias carpetas y archivos esenciales para la implementación del diseño responsivo. La estructura de directorios es la siguiente:

```
cfe_extracted/
│── cfe/
    │── css/
    │   │── bootstrap.min.css
    │   │── bootstrap-icons.css
    │   │── estilos.css
    │── js/
    │   │── bootstrap.bundle.min.js
    │   │── scripts.js
    │── index.html
    │── clientes.html
    │── comisionistas.html
    │── login.html
    │── mensajeria.html
    │── pagos.html
```

### 2. Uso de Frameworks CSS
El proyecto utiliza **Bootstrap** como el framework principal para la implementación del diseño responsivo. Se incluyen los siguientes archivos:
- `css/bootstrap.min.css`: Contiene los estilos predefinidos de Bootstrap para la maquetación responsiva.
- `css/bootstrap-icons.css`: Permite el uso de íconos de Bootstrap en la interfaz.
- `css/estilos.css`: Archivo de estilos personalizados adicionales para modificar el comportamiento responsivo según las necesidades del proyecto.

### 3. Aplicación del Diseño Responsivo
El diseño responsivo se implementa mediante varios enfoques:

#### a) Sistema de Rejilla de Bootstrap
Cada archivo HTML estructura su contenido utilizando el sistema de **grid** de Bootstrap. Ejemplo de su uso en un archivo HTML:
```html
<div class="container">
    <div class="row">
        <div class="col-md-6 col-sm-12">Contenido de la izquierda</div>
        <div class="col-md-6 col-sm-12">Contenido de la derecha</div>
    </div>
</div>
```
Aquí, `col-md-6` indica que en pantallas medianas o grandes, cada columna ocupará el 50% del ancho, mientras que en pantallas pequeñas (`col-sm-12`) cada columna ocupará el 100% del ancho.

#### b) Clases de Visibilidad
Se utilizan clases de Bootstrap para controlar la visibilidad de elementos según el tamaño de la pantalla:
```html
<div class="d-none d-md-block">Este texto solo se muestra en pantallas medianas o más grandes</div>
```
`d-none` oculta el contenido por defecto y `d-md-block` lo hace visible en dispositivos medianos en adelante.

#### c) Media Queries Personalizados
Además del uso de Bootstrap, el archivo `estilos.css` puede incluir media queries personalizadas para ajustes específicos:
```css
@media (max-width: 768px) {
    .custom-container {
        padding: 10px;
    }
}
```
Este código ajusta el `padding` del contenedor `.custom-container` en pantallas menores a 768px.

#### d) Componentes Flexibles
Se emplean clases como `d-flex`, `justify-content-center` y `align-items-center` para mejorar la alineación en diferentes dispositivos:
```html
<div class="d-flex justify-content-center align-items-center" style="height: 100vh;">
    <p>Texto centrado en la pantalla</p>
</div>
```

### 4. Referencias en los Archivos HTML
Cada archivo HTML incluye las referencias necesarias a Bootstrap dentro de la etiqueta `<head>`:
```html
<head>
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link rel="stylesheet" href="css/bootstrap-icons.css">
    <link rel="stylesheet" href="css/estilos.css">
</head>
```
Y los scripts de Bootstrap en el cierre del `body`:
```html
<script src="js/bootstrap.bundle.min.js"></script>
<script src="js/scripts.js"></script>
```

---
Este documento proporciona un desglose detallado sobre la estructura y aplicación del diseño responsivo en el proyecto.

