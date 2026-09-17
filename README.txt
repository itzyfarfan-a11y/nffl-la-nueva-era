NFFL LA NUEVA ERA — PAQUETE FINAL

Archivos:
- index.html: panel de Administración NFFL.
- roster.html: formulario de roster para el coach mediante enlace seguro.
- edge_index.ts: fuente Edge Function para servir el panel Admin.
- nffl-roster_index.ts: fuente Edge Function nffl-roster para servir el formulario de roster.
- portal_edge_index.ts: fuente Edge Function del portal público.
- public_edge_index.ts: copia equivalente del portal público.
- _headers: evita caché de los archivos estáticos.

Reglas principales ya integradas:
- Máximo 18 jugadores por roster.
- Nombre, foto y número de jersey obligatorios.
- CURP obligatoria para Mom’s y +35 Varonil.
- Números de jersey no duplicados dentro del mismo roster.
- El enlace de roster funciona mientras el torneo está en estado Próximo.
- Al activar el torneo se cierran los cambios de roster.
- Tabla: DIF → PA → PC.
- Incomparecencia: 18–0 y se conserva el adeudo de arbitraje.
- Sustitución de equipos y juegos de reposición.
- Playoffs adaptables a 2, 3, 4, 5, 6, 7 y 8+ equipos.
- Portal público muestra calendarios/resultados/playoffs publicados y rosters aprobados.

Antes de publicar, desplegar las Edge Functions con sus nombres correspondientes y conservar únicamente la clave publishable de Supabase en el cliente. Nunca incluir una service_role/secret key en estos archivos.

- Validación de resultados: solo acepta marcadores enteros de 0 o mayores.
- Validación de roster en cliente y servidor contra duplicidad de jersey.
