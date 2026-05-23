# SoftmpsTemplate

Template base Full Stack con:

- Backend ASP.NET Core Web API (.NET 8)
- Frontend Vue + Vite
- SQL Server
- Arquitectura organizada para proyectos reales

---

# Tecnologias utilizadas

## Backend
- .NET 8
- ASP.NET Core Web API
- C#
- SQL Server

## Frontend
- Vue
- Vite
- Node.js
- npm

## Herramientas
- VS Code
- Git
- SQL Server Management Studio (SSMS)

---

# Estructura del proyecto

```txt
SoftmpsTemplate/
│
├── backend/
│   ├── Controllers/
│   ├── Models/
│   ├── Negocio/
│   ├── Properties/
│   ├── StartupConfig/
│   ├── Utils/
│   ├── Program.cs
│   ├── appsettings.json
│   └── backend.csproj
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── database/
│
├── docs/
│
└── README.md
```

---

# Requisitos previos

Antes de ejecutar el proyecto necesitas instalar:

## Programas necesarios

### VS Code
Editor principal.

Descarga:
https://code.visualstudio.com/

---

### Git
Control de versiones.

Verificar instalación:

```bash
git --version
```

Descarga:
https://git-scm.com/downloads

---

### .NET 8 SDK

Verificar instalación:

```bash
dotnet --version
```

Descarga:
https://dotnet.microsoft.com/en-us/download

---

### SQL Server

Opciones recomendadas:

- SQL Server Developer
- SQL Server Express

Descarga:
https://www.microsoft.com/en-us/sql-server/sql-server-downloads

---

### SQL Server Management Studio (SSMS)

Herramienta visual para administrar bases.

Descarga:
https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms

---

### Node.js LTS

Verificar instalación:

```bash
node --version
npm --version
```

Descarga:
https://nodejs.org/

---

# Extensiones recomendadas para VS Code

Instalar:

- C# Dev Kit
- C#
- Vue - Official
- ESLint
- Prettier
- SQL Server
- GitLens

---

# Configuracion inicial del proyecto

## 1. Clonar repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

---

## 2. Abrir proyecto

```bash
cd SoftmpsTemplate
code .
```

---

# Configuracion Backend

Entrar a la carpeta backend:

```bash
cd backend
```

---

## Restaurar paquetes NuGet

```bash
dotnet restore
```

---

## Ejecutar backend

```bash
dotnet run
```

Salida esperada:

```txt
Now listening on: http://localhost:5000
Application started.
```

---

# Configuracion Frontend

Abrir otra terminal.

Entrar a frontend:

```bash
cd frontend
```

---

## Instalar dependencias

```bash
npm install
```

---

## Ejecutar frontend

```bash
npm run dev
```

Salida esperada:

```txt
VITE vX.X.X ready
Local: http://localhost:5173/
```

---

# Configuracion SQL Server

## Crear base de datos

Abrir SSMS y ejecutar:

```sql
CREATE DATABASE SoftmpsDB;
GO

USE SoftmpsDB;
GO
```

---

# Conexion Backend -> SQL Server

Modificar:

```txt
backend/appsettings.json
```

Ejemplo:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=SoftmpsDB;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
```

---

# Comandos utiles

## Backend

```bash
dotnet run
```

```bash
dotnet build
```

```bash
dotnet clean
```

---

## Frontend

```bash
npm run dev
```

```bash
npm run build
```

```bash
npm install
```

---

# GitIgnore

## Frontend ignora

- node_modules
- dist
- .env
- logs

## Backend ignora

- bin
- obj
- appsettings.Development.json
- .vs

---

# Flujo recomendado de desarrollo

## Backend
1. Crear Controller
2. Crear Models
3. Crear lógica en Negocio
4. Conectar SQL Server
5. Probar endpoints

---

## Frontend
1. Crear vistas
2. Crear componentes
3. Crear services API
4. Conectar backend
5. Manejar rutas

---

# Puertos comunes

| Servicio | Puerto |
|---|---|
| Backend .NET | 5000 / 5001 |
| Frontend Vite | 5173 |
| SQL Server | 1433 |

---

# Problemas comunes

## node no reconocido

Reinstalar Node.js LTS.

---

## dotnet no reconocido

Reinstalar .NET SDK.

---

## npm install falla

Eliminar:

```txt
node_modules
package-lock.json
```

Y ejecutar:

```bash
npm install
```

---

## Error conexion SQL

Verificar:

- SQL Server iniciado
- Nombre de instancia
- ConnectionString
- Puerto 1433

---

# Estado actual del template

- Backend configurado
- Frontend configurado
- SQL Server configurado
- GitIgnore configurado
- Vite funcionando
- API funcionando

---

# Autor

Proyecto base Full Stack para desarrollo rapido con:

- .NET
- Vue
- SQL Server
- Vite
- Arquitectura escalable