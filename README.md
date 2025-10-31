# Proyecto-2do-Departamental
🪴 Vivero Digital - Proyecto E-Commerce

Este es un proyecto de e-commerce completo construido con React, Vite, Supabase y TailwindCSS. La aplicación simula una tienda en línea de plantas y accesorios, permitiendo a los usuarios registrarse, navegar por el catálogo, añadir productos al carrito y finalizar un pedido de demostración.

 🚀 Tecnologías Utilizadas

* *Frontend:* React (con Vite)
* *Backend & DB:* Supabase (PostgreSQL)
* *Estilos:* TailwindCSS
* *Autenticación:* Supabase Auth (Email/Contraseña, Google & GitHub OAuth)
* *Storage:* Supabase Storage (para imágenes de productos)

 🏛 Arquitectura y Flujo

1.  *Autenticación:* El sistema maneja usuarios públicos (anon) y autenticados (authenticated). Se utilizan RLS (Row Level Security) en Supabase para proteger los datos.
2.  *Catálogo:* Los productos y categorías se cargan desde Supabase DB.
3.  *Carrito:* El estado del carrito se maneja globalmente con React Context.
4.  *Pedido Demo:* Al "Finalizar Pedido", la aplicación crea un nuevo registro en las tablas orders y order_items y descuenta el stock de la tabla products usando una función SQL de Supabase.

🛠 Configuración Local

Para correr este proyecto en tu máquina local, sigue estos pasos:

1.  *Clona el repositorio:*
    bash
    git clone [URL_DE_TU_REPO_DE_VIVERO]
    cd [NOMBRE_DEL_REPO]
    

2.  *Navega al frontend e instala dependencias:*
    bash
    cd frontend
    npm install
    

3.  *Configura las variables de entorno:*
    * Crea un archivo .env en la carpeta frontend.
    * Copia el contenido de .env.example y llénalo con tus propias llaves de Supabase. *Este proyecto no requiere llaves de Stripe.*

 **Variables de Entorno (frontend/.env):**
    env
    # Claves de Supabase
    VITE_SUPABASE_URL=tu_url_de_proyecto_supabase
    VITE_SUPABASE_ANON_KEY=tu_llave_anon_de_supabase
    

4.  *Corre el proyecto:*
    bash
    npm run dev
    

👨‍💻 Usuarios de Prueba

* *Email:* cliente4@tutienda.com
* *Contraseña:* 12345678
* (O usa el login social con Google/GitHub)
