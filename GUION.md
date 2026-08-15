Integrante 1 -
Integrante 2 -
Integrante 3 -
Integrante 4 -
Integrante 5 -
Integrante 6 -
Integrante 7 -

---

Integrante 1 — Problemática y justificación

Buenas tardes. A continuación presentaremos nuestro proyecto final: Casino Zero Trust, un laboratorio de privacidad y ciberseguridad.

La idea parte de algo simple: casi nadie lee los permisos que acepta en internet —cámara, ubicación, notificaciones, cookies porque los sitios los piden justo cuando uno quiere algo, y a veces con pretextos que no explican realmente para qué se van a usar.



Integrante 2 — Objetivos y alcance

El objetivo fue diseñar y desarrollar esta plataforma para mostrar, de forma ética y controlada, cómo funcionan los permisos del navegador y las cookies, aplicando buenas prácticas de seguridad y un módulo que concientice sobre privacidad digital.

Para lograrlo nos propusimos: aplicar Scrum en Jira con historias de usuario y al menos dos sprints, diseñar wireframes y mockups antes de programar, construir un backend con autenticación real, y un frontend que pida los cuatro permisos: cámara, micrófono, ubicación y notificaciones, siempre con consentimiento explícito.



Integrante 3 — Metodología ágil y Jira

Todo el trabajo lo organizamos con Scrum, en Jira. Armamos un backlog con las historias de usuario, cada una con su prioridad y su responsable asignado, y las repartimos en seis sprints: acceso y autenticación, privacidad y consentimiento, gestión de permisos, los juegos del casino, el dashboard de privacidad, y backend y seguridad.

El tablero se manejó con las columnas de siempre: por hacer, en curso, en revisión y finalizado. Al final las veinte actividades del proyecto quedaron completadas al cien por ciento, repartidas entre los siete integrantes según su carga de trabajo.

Esto nos ayudó a no perder el hilo en un proyecto con varias partes moviéndose al mismo tiempo: mientras unos hacían el backend, otros ya estaban armando los mockups o los juegos.

Integrante 4 — Diseño UX/UI

Antes de escribir una sola línea de interfaz, definimos cada pantalla con wireframes de baja fidelidad: bloques grises, sin color ni tipografía, solo para acomodar la estructura. Ahí decidimos cosas como el panel dividido de login y registro, o cómo se vería el dashboard de concientización.

Ya con la estructura aprobada, pasamos a mockups de alta fidelidad, con la identidad visual final del laboratorio: fondo oscuro, acentos en dorado y verde, para que se sintiera a casino sin dejar de verse serio.

Ese proceso lo aplicamos a las pantallas clave: inicio, login, registro, la sección de juegos secundarios, el dashboard de huella digital y el aviso de privacidad. Diseñar primero en baja fidelidad nos ahorró tener que rehacer pantallas completas ya avanzado el desarrollo.

Integrante 5 — Arquitectura y stack

El proyecto se divide en dos repositorios separados. El frontend, casino-app, está hecho con React 19, TypeScript y Vite, desplegado en Vercel. El backend, casino-backend, está hecho con NestJS, TypeORM y SQLite, desplegado en Railway. Se comunican entre sí por una API REST, mandando el token en cada petición protegida.



Integrante 6 — Modelo de datos

Diseñamos un modelo de datos completo de ocho tablas. De esas, tres ya están implementadas y funcionando en producción: users, que guarda cuenta y fichas; permission_events, la bitácora de cada permiso pedido, concedido o negado; y consent_records, las decisiones de cookies por sesión.

Las otras cinco —juegos, historial de jugadas, catálogo de cookies, versiones del aviso de privacidad y hallazgos de seguridad— ya las dejamos modeladas y documentadas, listas para las siguientes fases del laboratorio.



Integrante 7 — Seguridad

Del lado de seguridad aplicamos varias capas: límite de peticiones por minuto para evitar fuerza bruta, todas las consultas pasan por TypeORM para evitar inyección SQL, React escapa todo el contenido para evitar XSS, y validamos estrictamente cada dato que entra a la API. También dejamos documentados los riesgos que sí reconocemos, como guardar el token en localStorage en vez de una cookie httpOnly.

Integrante 1 — Pruebas

Para comprobar que todo esto funcionara de verdad, no solo en documentación, escribimos pruebas automatizadas con Jest y Supertest: dieciocho pruebas de integración y una unitaria, todas pasando, cada una con su caso positivo y sus casos negativos. Una de esas pruebas, sin buscarlo, nos confirmó que el límite de peticiones sí bloqueaba un sexto registro en el mismo minuto.

Integrante 2 — Despliegue

Y finalmente lo desplegamos en un entorno real: el backend en Railway y el frontend en Vercel, para poder mostrárselo tal cual funciona en producción, no solo en nuestras máquinas.

Con esto cerramos la parte de teoría. Ahora les vamos a hacer una demostración en vivo de Casino Zero Trust.


