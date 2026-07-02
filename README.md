# La Teoría del Puente — Web

Sitio estático para `lateoriadelpuente.com`, alojado en GitHub Pages.

---

## Estructura del repositorio

```
/
├── index.html     ← página principal (editar aquí)
├── CNAME          ← dominio personalizado (no tocar)
└── README.md      ← este archivo
```

---

## Cómo actualizar la bitácora

Abrir `index.html` y localizar la sección con el comentario `<!-- ══ BITÁCORA ═══ -->`.

Cada entrada sigue este patrón. Copiar y pegar arriba de las existentes (la más nueva va primero):

```html
<div class="entrada">
  <div class="entrada-fecha">Jul<br>2026</div>
  <div>
    <div class="entrada-tag">Principio</div>
    <div class="entrada-titulo">Título de la entrada</div>
    <p class="entrada-texto">
      Texto de la entrada. Puede ser tan largo como se necesite.
      Viene de un video de TikTok, un episodio del podcast,
      una reflexión de un proyecto.
    </p>
    <div class="entrada-origen">↳ Fuente: TikTok / YouTube / Caso en curso</div>
  </div>
</div>
```

**Etiquetas disponibles para `entrada-tag`:**
- `Principio` — ideas del sistema
- `Caso` — proyectos documentados
- `Fundamentos` — manifiesto, identidad
- `Por la Causa` — entradas del podcast / video
- `Herramienta` — recursos del método

---

## Configurar el dominio en GitHub Pages

1. Ir a **Settings → Pages** en el repositorio
2. En **Source**: rama `main`, carpeta `/` (raíz)
3. En **Custom domain**: escribir `lateoriadelpuente.com`
4. Activar **Enforce HTTPS**

En el registrador del dominio, agregar estos registros DNS:

```
Tipo A    @    185.199.108.153
Tipo A    @    185.199.109.153
Tipo A    @    185.199.110.153
Tipo A    @    185.199.111.153
Tipo CNAME www  tu-usuario.github.io
```

Tiempo de propagación: entre 10 minutos y 24 horas.

---

## Tipografía

Usa **IM Fell English** (Google Fonts, carga automática).
No requiere instalación ni archivos adicionales.

---

## Para agregar nuevas secciones en el futuro

El layout usa CSS Grid con áreas nombradas.
Cada sección nueva necesita:
1. Un `<section>` con `id` y clase CSS
2. Una línea en `grid-template-areas` en el CSS
3. Un enlace en el `<nav>`

Si el contenido crece mucho, considerar separar la bitácora
en archivos individuales y usar un generador estático
como Jekyll (compatible con GitHub Pages de forma nativa).
