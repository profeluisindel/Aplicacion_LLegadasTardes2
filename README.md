# Colegio La Pulida S.A.

Aplicación para administrar estudiantes, grados y llegadas tardías con una API Express, Prisma y PostgreSQL, y una interfaz React.

## Requisitos

- Node.js 20.19 o superior.
- PostgreSQL instalado y disponible localmente.

## Preparación

1. Instala las dependencias del backend: `npm ci`.
2. Instala las dependencias del FrontEnd: `npm ci --prefix FrontEnd`.
3. Copia `.env.example` a `.env` y configura `DATABASE_URL` con las credenciales locales.
4. Genera Prisma Client: `npm run db:generate`.
5. Aplica las migraciones: `npm run db:migrate`.

## Ejecución

Desde la raíz, `npm run dev` inicia la API y el servidor Vite al mismo tiempo. La API usa `http://localhost:3000` y Vite muestra su dirección local (por defecto `http://localhost:5173`).

También se pueden iniciar por separado:

- Backend: `npm start` o `npm run dev:api`.
- FrontEnd: `npm run dev:frontend` desde la raíz o `npm run dev` dentro de `FrontEnd/`.

La URL de la API del FrontEnd se configura con `VITE_API_URL` en `FrontEnd/.env`; su valor predeterminado es `http://localhost:3000/api`.
