# Intranet Frontend

Este proyecto es una aplicación frontend para el proyecto de Ingenieria de Software. Está construido usando Vue 3 y Vite, con Tailwind CSS para el estilo.

## Estructura del Proyecto

- `src/components`: Contiene los componentes de Vue utilizados en toda la aplicación.
- `src/views`: Contiene las vistas principales de la aplicación (Aqui deben ir solo las paginas).
- `src/App.vue`: El componente raíz.
- `src/main.js`: El punto de entrada de la aplicación.
- `tailwind.config.js`: Archivo de configuración para Tailwind CSS.
- `index.html`: El archivo HTML principal.
- `package.json`: Archivo de configuración de npm.

## Configuración del Proyecto

1. Clona el repositorio:
    ```sh
    git clone https://github.com/tu-repo/intranet-frontend.git
    cd intranet-frontend
    ```

2. Instala las dependencias (`El proyecto ya cuenta con axios y vue-router`):
    ```sh
    npm install
    ```

## Desarrollo

### Compilar para Desarrollo

Para iniciar el servidor
```sh
npm run dev
```

## Componentes

### SideBar

El componente `SideBar` se utiliza para mostrar el menú de navegación. Incluye un botón de alternancia para abrir y cerrar la barra lateral.

### Notifications

El componente `Notifications` muestra íconos para el chat y las notificaciones con indicadores.

### HomeContent

El componente `HomeContent` muestra el contenido principal de la vista de inicio.

## Agregar Nuevos Componentes

1. Crea un nuevo componente en el directorio `src/components`.
2. Importa y usa el componente en la vista relevante u otro componente y asegurate de importar la ruta en `src/router/index.js`.

## Estilos

Este proyecto utiliza Tailwind CSS. Puedes agregar estilos personalizados en el archivo `src/index.css` o directamente en los componentes usando clases de utilidad de Tailwind.
