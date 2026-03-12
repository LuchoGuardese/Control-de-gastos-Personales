<div align="center">

# Control de Gastos Personales

Aplicación web para registrar, visualizar y gestionar ingresos y egresos personales, con balance general y filtros avanzados.

</div>

---

## Integrantes

- Burgos, Belén  
- Guardese, Iván  
- Guardese, Luciano  
- Hubert, Noelia  
- Ibáñez, Ian Franco  

---

## Tecnologías utilizadas

- **Frontend**: React 18 (PUERTO 3000)  
- **Backend**: Express + Sequelize (API REST, PUERTO 3001)  
- **Base de datos**: PostgreSQL 15 (PUERTO 5433)  
- **Cache y sesiones**: Redis 7 (PUERTO 6379)  
- **Proxy reverso**: Nginx (PUERTO 80)  
- **Administración de BD**: pgAdmin 4 (PUERTO 5050)  

---

## Características principales

- **Registro de usuarios** con persistencia en base de datos.
- **Inicio de sesión** y acceso a un **panel principal**.
- **Listado de movimientos** con ejemplos de ingresos y egresos.
- **Balance general** visible y actualizado.
- **ABM de movimientos**: editar y eliminar cada movimiento.
- **Filtros por categoría y fecha** para personalizar el balance.
- **Alta de nuevos movimientos** indicando tipo (Ingreso o Egreso), categoría, monto, etc.

---

## Requisitos previos

Asegurate de tener instalado:

- **Git**
- **Docker** y **Docker Compose**

---

## Instalación y puesta en marcha

1. **Clonar el repositorio**

   ```bash
   git clone https://github.com/belenburgos20/Programaci-n-3.git
   cd "Programaci-n-3/Proyecto-Final"
   ```

2. **Configurar variables de entorno**

   ```bash
   cp .env.template .env
   ```

   Luego, si es necesario, ajustá los valores del archivo `.env` (puertos, credenciales, etc.).

3. **Levantar los contenedores**

   ```bash
   docker-compose up -d
   docker-compose ps
   ```

4. **Aplicar migraciones y datos de prueba**

   ```bash
   docker exec -it app_backend npm run migrate
   docker exec -it app_backend npm run seed
   ```

---

## Acceso a la aplicación

- **Frontend**: `http://localhost:3000`
- **Backend (API)**: `http://localhost:3001`
- **pgAdmin**: `http://localhost:5050`

---

## Usuario de prueba

Podés ingresar con el siguiente usuario de ejemplo:

- **Usuario**: `administrador@test.com`  
- **Contraseña**: `123456`

---

## Uso de la aplicación

1. Si no tenés cuenta, registrate desde la pantalla de inicio ingresando **nombre**, **correo** y **contraseña**.  
2. El registro guarda los datos en la base de datos y te redirige automáticamente al **login**.  
3. Una vez iniciada la sesión, accederás al **menú principal**, donde vas a encontrar:
   - Movimientos de ejemplo (ingresos y egresos).
   - Balance general visible.
   - Botones para **editar** o **eliminar** cada movimiento.
   - Filtros por **categoría** y **fecha** para personalizar el balance.
4. En la parte superior del listado hay un **formulario** para ingresar nuevos movimientos, seleccionando el tipo (**Ingreso** o **Egreso**) y completando los datos necesarios.

---

## Estado del proyecto

Proyecto desarrollado como **trabajo final** de la materia **Programación 3 (UTN)**.
