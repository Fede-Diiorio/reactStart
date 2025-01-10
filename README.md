# Guía para configurar un proyecto con Vite/React

## Instalación de Vite/React para un proyecto

1. **Consultar la documentación oficial**

   - Ingresa al sitio de Vite: [Vite Guide](https://vitejs.dev/guide/)
   - Busca la sección para React con JavaScript.

2. **Ejecutar los comandos en consola**

   ```bash
   npm create vite@latest
   ```

   - Ingresa el nombre del proyecto.
   - Selecciona el framework: `React`.
   - Selecciona la variante: `JavaScript`.

3. **Cambiar al directorio del proyecto y finalizar la instalación**

   ```bash
   cd nombreDelProyecto
   npm install
   ```

4. **Correr el servidor de desarrollo**
   ```bash
   npm run dev
   ```

---

## Instalación de SASS en un proyecto Vite/React

1. **Instalar SASS y sass-loader**

   ```bash
   npm install -D sass sass-loader
   ```

2. **Configurar Vite para usar SCSS**

   - Asegúrate de configurar el archivo `vite.config.js` para manejar archivos SCSS.
   - Ejemplo de configuración:

     ```javascript
     import { defineConfig } from "vite";
     import react from "@vitejs/plugin-react";

     export default defineConfig({
       plugins: [react()],
       css: {
         preprocessorOptions: {
           scss: {
             additionalData: `
               @import url('https://fonts.googleapis.com/css2?family=Lato&family=Prompt:wght@400;700&display=swap');
               $primaryFont: 'Prompt', sans-serif;
               $secondaryFont: 'Lato', sans-serif;
               $primary: #35A7FF;
               $darkPrimary: #004777;
               $secondary: #FFE74C;
               $darkSecondary: #D5B800;
               $assistant: #C2FCF7;
               $white: #ffffff;
               $black: #000000;
               $grey: #b1adad;
               $darkGrey: #3d3d3d;
               $delete: #d61d16;
               $darkDelete: #8a130f;
             `,
           },
         },
       },
     });
     ```

---

## Instalación de Bootstrap en un proyecto Vite/React

1. **Instalar Bootstrap**

   ```bash
   npm install bootstrap
   ```

2. **Importar los estilos en `main.jsx`**
   ```javascript
   import "bootstrap/dist/css/bootstrap.min.css";
   ```

---

## Integrar íconos de FontAwesome al proyecto

1. **Instalar la librería React-Icons**

   ```bash
   npm install react-icons
   ```

2. **Buscar el ícono requerido**

   - Consulta el repositorio de íconos: [React Icons](https://react-icons.github.io/react-icons/icons/fa6/)

3. **Importar y utilizar el ícono**

   ```javascript
   import { FaAnchor } from "react-icons/fa6";

   function MyComponent() {
     return <FaAnchor className="icon-class" />;
   }
   ```

---

## Vincular un proyecto con un repositorio de GitHub

1. **Inicializar Git y conectar con GitHub**
   ```bash
   git init
   git add README.md
   git commit -m "first commit"
   git branch -M main
   git remote add origin nombreDelRepositorio
   git push -u origin main
   ```

---

## Instalación de librerías para routing y navegación

1. **Instalar React Router DOM**

   ```bash
   npm i react-router-dom
   ```

2. **Componentes clave para el ruteo**
   - **`BrowserRouter`**: Envuelve a los componentes que requieren navegación.
   - **`Routes`**: Agrupa componentes que serán renderizados condicionalmente.
   - **`Route`**: Define qué componentes se montan según la URL.
   - **`Link`**: Crea enlaces para navegar dentro de la aplicación.
   - **`useParams` (hook)**: Obtiene parámetros de la URL.

---
