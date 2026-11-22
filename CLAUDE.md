# TIMP Tecnologías — Landing page

Contexto para Claude Code. Leelo antes de hacer cambios.

## Qué es
Landing page de **TIMP Tecnologías**, emprendimiento de 4 personas (trabajo remoto, sin roles fijos) que ofrece páginas web, automatizaciones (asistentes de WhatsApp/Telegram, n8n, agentes con IA) y software a medida a pymes y emprendedores de Argentina.

- Repo: https://github.com/TobiiC/TIMP-landing-page
- Hosting: Vercel (proyecto importado desde GitHub, framework "Other", sin build). Cada push a `main` publica.
- Modelo: igual que el portfolio de Tobias (https://github.com/TobiiC/Portfolio): HTML + CSS puro, carpeta `images/`.

## Estructura
```
index.html     Contenido (secciones: hero, ¿Te suena?, servicios, asistente de cobros, cómo trabajamos, preguntas, contacto)
style.css      Estilos. Colores y fuentes en :root
favicon.ico    Ícono (la P con circuitos del logo, fondo navy)
images/        logo-navy.png, logo-blanco.png, oficina.jpg, comercio.jpg, celular.jpg,
               og-image.jpg (1200x630, vista previa en redes), favicon-32.png, apple-touch-icon.png, icon-512.png
```
Sin frameworks, sin npm, sin build. Mantenerlo así salvo que Tobias pida otra cosa.
Para verlo local: abrir `index.html` o `npx serve .`

## Marca
| Token | Valor |
|---|---|
| Navy | `#123152` (titulares, logo, fondos oscuros) |
| Azul acento | `#2E61C0` (botones, palabra destacada "impulsan", íconos) |
| Azul claro | `#9DB8EC` (detalles sobre fondo navy) |
| Fondo suave | `#F3F5F8` |
| Gris texto | `#5B6170` |

- Tipografía: Montserrat (Google Fonts), titulares 800.
- Eslogan: "Creamos soluciones que impulsan tu negocio."
- Pilares: Confianza · Compromiso · Resultados.
- Nombre siempre "TIMP Tecnologías" (plural, con tilde).
- Íconos: SVG inline de trazo, nunca emoji.

## Reglas de contenido
- Español rioplatense (vos), tono cercano y profesional, sin tecnicismos: hablar del dolor del cliente (tiempo, desorden, control), no de la tecnología.
- **No inventar** precios, testimonios, clientes, cifras ni teléfonos. Todavía no tienen clientes.
- Asistente de cobros: decir "asistente de cobros" o "avisos de cobro en tiempo real" (no "bot"); "en segundos", nunca "instantáneo garantizado"; solo consulta movimientos y avisa, no hace transferencias; no nombrar bancos ni billeteras.

## Decisiones tomadas
- Contacto: **solo mail (timptecnologias@gmail.com) e Instagram (@timp.tecnologias)**. Sin WhatsApp ni LinkedIn por ahora.
- **Sin sección de proyectos/portfolio** por ahora (no hay capturas). Proyectos que podrían sumarse después: notificador de transferencias, e-commerce de un entrenador personal.
- Público ampliado: pymes, emprendedores y empresas. Los dolores se cuentan como procesos (no escenas de mostrador) y el asistente de cobros se presenta como un ejemplo, no como el producto principal.
- Repo público.
- Vercel plan Hobby por ahora. Ojo: el Hobby es para uso no comercial; si facturan o Vercel lo pide, pasar a Pro o mover a otro hosting (Cloudflare Pages / Netlify).

## Pendientes
- Cuando esté el dominio de Vercel, poner la URL **absoluta** en `og:image` (y agregar `og:url`): WhatsApp no muestra la vista previa con rutas relativas.
- Si consiguen dominio propio, configurarlo en Vercel y actualizar las URLs.

## Accesibilidad y calidad
- Contraste de texto mínimo 4.5:1; botones y links de al menos 44px de alto.
- Probar a 390px (celular) y 1440px. El menú se vuelve hamburguesa por debajo de 860px.
- Respetar `prefers-reduced-motion`.
