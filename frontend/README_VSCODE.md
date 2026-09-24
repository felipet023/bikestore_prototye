# Cómo abrir este proyecto en Visual Studio Code

## 1. Descomprimir

Descomprime `frontend-crud.zip` en una carpeta de tu computador.

## 2. Abrir la carpeta correcta

En Visual Studio Code selecciona **Archivo → Abrir carpeta** y elige la carpeta llamada `frontend`.

Debes ver estos archivos en el explorador:

- `package.json`
- `index.html`
- `vite.config.js`
- `src/`

No abras solamente un archivo `.jsx`; debes abrir la carpeta completa del proyecto.

## 3. Abrir la terminal

En VS Code selecciona **Terminal → Nueva terminal** y ejecuta:

```bash
npm install
```

Este comando instala las dependencias dentro de `node_modules`. Esa carpeta no se incluye en el ZIP porque se genera automáticamente.

## 4. Iniciar el proyecto

Después de instalar las dependencias, ejecuta:

```bash
npm run dev
```

Abre en el navegador la dirección que muestre la terminal, normalmente:

```text
http://localhost:5173
```

## Requisitos

- Node.js 20 o superior.
- npm instalado.
- El backend debe estar ejecutándose en `http://localhost:3000` para que login y CRUD funcionen.

La variable de conexión está en `.env.development`:

```env
VITE_API_URL=http://localhost:3000/api
```

Si solamente quieres comprobar que la interfaz abre, puedes ejecutar `npm run dev` aunque el backend todavía no esté iniciado. Las operaciones de login y equipos necesitarán el backend.

## Si aparece un error de dependencias

Desde la terminal ubicada en la carpeta `frontend`, ejecuta:

```bash
rm -rf node_modules package-lock.json
npm install
npm run dev
```

En Windows PowerShell, usa:

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item package-lock.json
npm install
npm run dev
```

## Comprobar compilación

Para validar que el código compila, ejecuta:

```bash
npm run build
```

El resultado correcto termina con un mensaje parecido a `built in ...`.
