## 🔑 Integración con Supabase

Este proyecto utiliza Supabase para la base de datos y la autenticación. Sigue estos pasos para configurar tu conexión:

1. **Instala la plantilla de autenticación** (si usas Breeze/Jetstream):

   ```
   composer require laravel/breeze --dev
   php artisan breeze:install
   ```

2. **Configura los detalles de conexión de Postgres**:

   - Ve al panel de control de tu proyecto en Supabase y crea una nueva base de datos.

   - Copia la cadena de conexión para el **Session Pooler**.

   - En tu archivo `.env`, actualiza los detalles de conexión a la base de datos. La URL completa se puede pegar directamente en la variable `DB_URL`:

     ```
     DB_CONNECTION=pgsql
     DB_URL="postgresql://user:password@hostname:port/database?options"
     ```

   - **Ejemplo**: `DB_URL="postgresql://postgres.xxxx:password@xxxx.pooler.supabase.com:5432/postgres"`

3. **Ejecuta las migraciones de la base de datos**:

   ```
   php artisan migrate
   ```

4. **Inicia la aplicación**:

   ```
   php artisan serve
   ```

## 