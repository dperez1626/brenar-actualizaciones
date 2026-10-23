# Actualizaciones de Brenar Lácteos

Este repositorio público contiene únicamente archivos para distribuir actualizaciones. El código fuente y las claves de firma deben mantenerse privados.

## Estado

Preparación inicial. Todavía no se ha publicado ni comprobado un APK de actualización. `update.example.json` es una plantilla y no anuncia una versión disponible.

## Publicar una versión

1. Compilar el APK conservando el identificador de aplicación y la firma de la versión instalada. Aumentar versionCode en cada nueva entrega.
2. Probar la actualización sobre una instalación existente y comprobar que conserva ventas y configuración.
3. En Releases, crear una entrega con su APK firmado. Usar su enlace real de descarga.
4. Copiar update.example.json como update.json en la raíz de main, con los valores reales de versionCode, versionName, apkUrl y releaseNotes. Publicar primero el APK y después el JSON.
5. En Settings > Pages, seleccionar Deploy from a branch, main y /(root), y guardar. Comprobar que https://dperez1626.github.io/brenar-actualizaciones/update.json devuelve directamente el JSON por HTTPS antes de configurar la app.
6. Configurar UPDATE_MANIFEST_URL con esa dirección al compilar la app que incorpora el actualizador. Esa primera versión requiere instalación manual una vez.

## Protección de datos

No subir .env, claves de firma, contraseñas, datos de clientes ni el proyecto fuente. El APK será público. La instalación de futuras versiones requiere la confirmación del usuario en Android.
