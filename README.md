# MUJER MAGNÉTICA™ — App de 21 días

Web app en React + Vite, lista para publicar como repositorio de GitHub y desplegar en Vercel, Netlify o un hosting estático.

## Funciona hoy
- 21 días reales extraídos de la guía principal, con práctica, pregunta y afirmación.
- Completado de días y barra de progreso.
- Diario personal con guardado automático **local en el navegador**.
- Exportación e importación de notas en JSON.
- Biblioteca con guía y workbook originales.
- Interfaz responsive y PWA instalable (según compatibilidad del navegador).
- Sección de 7 audios con reproductores preparados.
- Catálogo de 4 bonos.

## Falta para poder vender la promesa completa
1. **Audios:** agregar archivos propios MP3 `public/audio/audio-1.mp3` ... `audio-7.mp3` y comprobar sus reproductores.
2. **Bonos:** confirmar derechos de reventa y crear/seleccionar ediciones revisadas. Los PDF subidos por el usuario NO se empaquetaron en este repositorio público. Después subir los archivos a `public/materiales/` y enlazarlos en `src/main.jsx`.
3. **Acceso de compradoras:** esta demo NO tiene inicio de sesión ni control de acceso. Cualquiera que conozca la URL podrá abrirla. Para lanzamiento pago implementar autenticación + autorización Hotmart verificada en backend, por ejemplo Supabase Auth + Edge Function con validación de webhook y registros de compra. **Nunca** colocar el token secreto de Hotmart en React o GitHub público.
4. **Datos de usuarias:** en esta versión las notas están en localStorage del dispositivo; no se sincronizan. Para cuentas reales, crear tablas con RLS, consentimiento, exportación y eliminación de datos.
5. **QA:** revisar copys, páginas PDF, garantías y permisos antes de publicar.

## Ejecutar localmente
```bash
npm install
npm run dev
```

## Compilar
```bash
npm run build
```

## Subir a GitHub
Crear repositorio vacío en github.com y desde esta carpeta ejecutar:
```bash
git init
git add .
git commit -m "Primera versión de Mujer Magnética"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/mujer-magnetica-app.git
git push -u origin main
```

## Publicar
En Vercel, elegir `Add New → Project → Import Git Repository`, seleccionar el repositorio, framework `Vite`, `Build command: npm run build`, `Output directory: dist`. No requiere variables de entorno para esta primera versión.

## Nota de seguridad y marketing
No compartir una URL pública como “app exclusiva” hasta configurar la autorización de compras. No vender audios ni bonos como entregados hasta que efectivamente lo estén.
