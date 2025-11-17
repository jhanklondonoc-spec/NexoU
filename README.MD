# 📘 Plataforma Educativa NexoU - HTML y CSS (MPA)

Este proyecto replica el prototipo de la plataforma educativa **NexoU**, estructurado como una **Aplicación de Múltiples Páginas (MPA)**. Está construido con **HTML5** y **CSS3** sin frameworks, simulando una experiencia institucional moderna y funcional.

## 🎨 Diseño y Estilo

El diseño se inspira en el prototipo de [NexoU](https://login-cargo-13859023.figma.site/), siguiendo estos principios:

- **Estética institucional:** Uso de logotipo, colores corporativos y estructura clara.
- **Minimalismo funcional:** Formularios centrados, sin distracciones visuales.
- **Paleta institucional:** Tonos azules, dorados y blancos, con acentos suaves.
- **Tipografía limpia:** Fuente sans-serif moderna, idealmente
- **Componentes modulares:** Botones, campos y enlaces reutilizables.

## 🛠️ Stack Tecnológico

- **HTML5:** Estructura semántica para formularios, navegación y contenido.
- **CSS3:** Estilos responsivos, centrado vertical, botones y campos estilizados.

## 📂 Estructura de Archivos

```plaintext
proyecto-nexou/
├── index.html
├── README.MD
├── mockup/
│   ├── biblioteca.png
│   ├── index.png
│   ├── inicio.png
│   ├── perfil.png
│   ├── reservas.png
│   ├── soporte.png
│   └── tecnologia.png
├── src/
│   ├── html/
│   │   ├── inicio.html
│   │   ├── mis-reservas.html
│   │   ├── perfil.html
│   │   ├── recursos-biblioteca.html
│   │   ├── recursos-tecnologicos.html
│   │   └── soporte.html
│   ├── css/
│   │   ├── index.css
│   │   ├── inicio.css
│   │   ├── mis-reservas.css
│   │   ├── perfil.css
│   │   ├── recursos-biblioteca.css
│   │   ├── recursos-tecnologicos.css
│   │   └── soporte.css
├── images/
│   ├── computadora-portatil.png
│   ├── cuadrado-pagina-inicio-azul.png
│   ├── icono-audifono.png
│   ├── icono-camara.png
│   ├── icono-cpu.png
│   ├── icono-estrellas.png
│   ├── icono-lapiz.png
│   ├── icono-monitor.png
│   ├── icono-reloj.png
│   ├── icono-soporte.png
│   ├── icono-telefono.png
│   ├── imagen-perfil.png
│   ├── libro-abierto.png
│   └── ... (otros íconos PNG)
```

## 🗺️ Arquitectura de Páginas

```markdown
## 🗺️ Arquitectura de Páginas (MPA) - NexoU

La navegación se gestiona a través de enlaces directos a los diferentes archivos HTML, con una barra de navegación lateral consistente en todas las vistas (excepto en login).

### 1. `login.html` (Inicio de Sesión)

* **Ruta:** `/login.html` (Raíz del proyecto)
* **Propósito:** Página de autenticación para acceder a la plataforma educativa.
* **Contenido:** 
    * Logo de NexoU centrado
    * Título "Iniciar Sesión"
    * Subtítulo "Accede a tu plataforma educativa"
    * Campo de entrada: "Usuario o Email"
    * Campo de entrada: "Contraseña" (con opción de mostrar/ocultar)
    * Checkbox: "Recordarme"
    * Enlace: "¿Olvidaste tu contraseña?"
    * Checkbox opcional: "Acceso de Administrador"
    * Botón principal: "Iniciar Sesión"
    * Enlace inferior: "¿No tienes cuenta? Crear Cuenta"
    * Enlace de ayuda: "¿Necesitas ayuda? Contacta a soporte"
* **Navegación:** Al autenticarse exitosamente, redirige a `index.html`

---

### 2. `index.html` (Dashboard / Inicio)

* **Ruta:** `/index.html` o `/src/html/index.html`
* **Propósito:** Panel principal después del login. Vista de bienvenida con resumen de la plataforma.
* **Contenido:**
    * **Banner destacado amarillo:** "Reserva fácil y rápida" con descripción sobre acceso a libros y equipos tecnológicos
    * Dos botones CTA: "Ver Biblioteca" y "Ver Tecnología"
    * **Métricas del sistema (4 tarjetas):**
        * 156 Recursos Disponibles
        * 3 Reservas Activas
        * 2h Tiempo Promedio
        * +15% Popularidad
    * **Sección "Recursos Populares":** Lista de recursos destacados (Libros de Borís, Laptops Institucionales) con botón "Ver más"
    * **Widget "Calendario":** Muestra calendario mensual (Noviembre 2025)
    * **Sección "Próximas Reservas":** Lista de próximas reservas confirmadas (MacBook Pro, Sala de Conferencias, Proyector Epson) con botón "Ver todas"
    * **Sección "Anuncios Importantes":** Notificaciones relevantes (Mantenimiento Programado, Nuevos Recursos)
* **Navegación lateral:** Logo NexoU, menú con Inicio (activo), Biblioteca, Tecnología, Reservas (badge "3"), Perfil, Soporte, usuario DSFSFA, Cerrar Sesión

---

### 3. `biblioteca.html` (Catálogo de Biblioteca)

* **Ruta:** `/src/html/biblioteca.html`
* **Propósito:** Vista del catálogo completo de libros y recursos académicos disponibles.
* **Contenido:**
    * Título principal: "Catálogo de Biblioteca"
    * Subtítulo: "Explora nuestra colección de libros académicos y recursos de estudio"
    * Barra de búsqueda: "Buscar por título, autor o ISBN..."
    * Filtro dropdown: "Todas las categorías"
    * Indicador: "Mostrando 4 de 4 recursos"
    * **Grid de libros (tarjetas):** Cada tarjeta incluye:
        * Imagen del libro (placeholder de libro abierto)
        * Badge de estado: "Disponible", "Reservado", o sin badge
        * Título del libro
        * Autor (ej. "por María González")
        * Calificación con estrellas (ej. 4.5 ⭐)
        * Etiqueta de categoría (ej. "Tecnología", "Arte", "Ciencias", "Psicología")
        * Descripción breve
        * ISBN
        * Ubicación física (ej. "Piso 2, Sección A-15")
        * Disponibilidad
        * Botón "Reservar" (azul oscuro) o "No disponible" (gris)
        * Icono de ojo para ver detalles
    * **Libros mostrados:**
        * Fundamentos de Programación
        * Historia del Arte Moderno
        * Matemáticas Avanzadas
        * Psicología Organizacional
* **Navegación lateral:** Igual que index.html pero con "Biblioteca" activo

---

### 4. `tecnologia.html` (Recursos Tecnológicos)

* **Ruta:** `/src/html/tecnologia.html`
* **Propósito:** Catálogo de equipos tecnológicos disponibles para préstamo académico.
* **Contenido:**
    * Título principal: "Recursos Tecnológicos"
    * Subtítulo: "Equipos tecnológicos disponibles para uso académico y proyectos"
    * Barra de búsqueda: "Buscar equipos por nombre o especificaciones..."
    * Filtro dropdown: "Todas las categorías"
    * **Tarjetas de conteo (4 categorías):**
        * 5 Laptops
        * 3 Tablets
        * 0 Proyectores
        * 29 Total Disponible
    * Indicador: "Mostrando 6 de 6 equipos"
    * **Grid de equipos (tarjetas):** Cada tarjeta incluye:
        * Imagen del equipo
        * Badge de estado: "4 disponibles", "3 disponibles", "No disponible", "2 disponibles"
        * Nombre del equipo
        * Especificaciones técnicas (ej. "M2 Chip, 8GB RAM, 256GB SSD")
        * Descripción breve del uso
        * Duración máxima (ej. "4 horas")
        * Disponibilidad (fracción, ej. "5/8")
        * Próximo disponible (fecha y hora si aplica)
        * Botón "Reservar" (azul oscuro) o "Lista de espera" (gris)
    * **Equipos mostrados:**
        * MacBook Pro 13"
        * iPad Pro 11"
        * Proyector Epson (No disponible)
        * Monitor Dell 24"
        * Audífonos Sony WH-1000XM5
        * Cámara Canon EOS
* **Navegación lateral:** Igual que index.html pero con "Tecnología" activo

---

### 5. `reservas.html` (Mis Reservas)

* **Ruta:** `/src/html/reservas.html`
* **Propósito:** Gestión de reservas activas e historial de préstamos del usuario.
* **Contenido:**
    * Título principal: "Mis Reservas"
    * Subtítulo: "Gestiona tus reservas activas e historial de préstamos"
    * **Tarjetas de resumen (3 métricas):**
        * 3 Reservas Activas
        * 12 Completadas este mes
        * 1 Pendiente de confirmación
    * **Pestañas de navegación:**
        * "Reservas Activas" (activa)
        * "Historial"
    * **Listado de reservas activas:** Cada ítem incluye:
        * Imagen del recurso
        * Nombre del recurso
        * Código (ej. "Código: R2024-001")
        * Fecha
        * Horario
        * Ubicación
        * Badge de estado: "Confirmada", "Activo", "Pendiente"
        * Botones de acción: "Ver detalles" + "Extender" / "Renovar" + "Devolver" / "Cancelar" + "Confirmar"
    * **Reservas mostradas:**
        * MacBook Pro 13" (Confirmada) - Hoy, 14:00-18:00, Biblioteca Central Piso 2
        * Fundamentos de Programación (Activo) - 15 Sep, Hasta 22 Sep, Préstamo domiciliario
        * Proyector Epson (Pendiente) - Mañana, 10:00-13:00, Aula 205
    * **Sección "Acciones Rápidas":** 4 botones grandes:
        * Reservar Libro
        * Reservar Equipo
        * Ver Calendario
        * Extender Préstamo
* **Navegación lateral:** Igual que index.html pero con "Reservas" activo (badge "3" visible)

---

### 6. `perfil.html` (Mi Perfil)

* **Ruta:** `/src/html/perfil.html`
* **Propósito:** Gestión de información personal y configuración de cuenta del usuario.
* **Contenido:**
    * Título principal: "Mi Perfil"
    * Subtítulo: "Gestiona tu información personal y configuración de cuenta"
    * **Pestañas de navegación:**
        * "Información" (activa)
        * "Actividad"
        * "Configuración"
    * **Panel izquierdo (tarjeta de perfil):**
        * Foto de perfil (circular, imagen de usuario)
        * Nombre: "María Elena González"
        * ID de estudiante: "ID: 20240156"
        * Badge de estado: "Activo"
        * Email: maria.gonzalez@universidad.edu.co
        * Teléfono: +57 300 123 4567
        * Programa: Ingeniería de Sistemas
        * Semestre: 8° Semestre
        * Botón: "Editar Perfil"
    * **Panel derecho - Sección "Información Personal":**
        * Nombre completo: María Elena González
        * ID de estudiante: 20240156
        * Correo electrónico: maria.gonzalez@universidad.edu.co
        * Teléfono: +57 300 123 4567
        * Programa académico: Ingeniería de Sistemas
        * Semestre actual: 8° Semestre
        * Fecha de ingreso: Febrero 2021
        * Estado: Activo
    * **Sección "Estadísticas de Uso":**
        * Total de reservas: 47
        * Reservas activas: 3
        * Este mes: 12
        * Categoría favorita: Tecnología
        * Tiempo promedio: 3.2 horas
        * Puntualidad: 96% (badge azul)
* **Navegación lateral:** Igual que index.html pero con "Perfil" activo

---

### 7. `soporte.html` (Soporte y Ayuda)

* **Ruta:** `/src/html/soporte.html`
* **Propósito:** Centro de ayuda con preguntas frecuentes y formulario de contacto.
* **Contenido:**
    * Título principal: "Soporte y Ayuda"
    * Subtítulo: "Encuentra respuestas a tus preguntas y obtén ayuda cuando lo necesites"
    * **Pestañas de navegación:**
        * "Preguntas Frecuentes" (activa)
        * "Contacto"
        * "Guías"
        * "Crear Ticket"
    * Barra de búsqueda: "Buscar en preguntas frecuentes..."
    * **Sección "Reservas" (acordeón expandible):**
        * ¿Cómo puedo reservar un libro?
        * ¿Cuánto tiempo puedo tener un libro prestado?
        * ¿Puedo cancelar una reserva?
        * ¿Qué pasa si llego tarde a recoger mi reserva?
    * **Sección "Equipos Tecnológicos" (acordeón expandible):**
        * ¿Qué equipos están disponibles para reservar?
        * ¿Por cuánto tiempo puedo usar un equipo?
        * ¿Qué hago si un equipo se daña durante mi préstamo?
    * **Sección "Cuenta y Perfil" (acordeón expandible):**
        * ¿Cómo actualizo mi información personal?
        * ¿Cómo cambio mi contraseña?
* **Navegación lateral:** Igual que index.html pero con "Soporte" activo

---

## 📋 Navegación Global

**Menú lateral presente en todas las páginas (excepto login):**
- Logo NexoU (arriba)
- Inicio (icono casa)
- Biblioteca (icono libro)
- Tecnología (icono computadora)
- Reservas (icono calendario) - con badge numérico "3"
- Perfil (icono persona)
- Soporte (icono ayuda/interrogación)


**Flujo de navegación principal:**
1. Usuario ingresa por `login.html`
2. Al autenticarse, accede a `index.html` (Dashboard)
3. Desde el dashboard puede navegar a cualquier sección mediante el menú lateral
4. Todas las páginas mantienen el mismo menú de navegación para facilitar el acceso
```

## 🎨 Paleta de Colores

* **Blanco:** `#FFFFFF`  
* **Azul Marino Oscuro:** `#011A42`  
* **Mostaza Dorado:** `#D49D28`  
* **Amarillo Arena Suave:** `#F8CD86`  
* **Gris Metálico Claro:** `#CFCFCF`  
* **Azul Intenso:** `#284693`  
* **Azul Pastel Grisáceo:** `#A6A9BB`  
* **Azul Marino Medio:** `#0A387A`  
* **Marrón Tierra:** `#AA700F`  
* **Negro:** `#000000`


## ✒️ Tipografía

- **Fuente principal:** `montserrat`,`poppins`,`Avenir Next Arabic`,`Mukti`
- **Importación:** vía Google Fonts


