# 🎬 Plataforma de Historias Épicas - Experiencia Cinematográfica

Una plataforma web interactiva que presenta 10 historias históricas con contenido multimedia, quizzes interactivos y una experiencia cinematográfica envolvente.

![Historias Épicas](https://img.shields.io/badge/Historias-10-gold)
![Preguntas Quiz](https://img.shields.io/badge/Preguntas-50-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.6-blue)
![React](https://img.shields.io/badge/React-19-blue)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.1-blue)

## 📋 Características

✨ **10 Historias Épicas**
- La Batalla de Maratón (490 a.C.)
- Nerón - Déspota y Artista (37-68 d.C.)
- Rey Arturo - El Mito de Camelot
- Esparta - Ciudad de Guerreros
- Batalla de Waterloo (1815)
- Buda - El Hombre que Iluminó el Mundo
- Cleopatra - La Última Reina de Egipto
- Templarios - Los Caballeros de la Cruz
- Príncipe Don Carlos - Un Destino Trágico
- Calígula - Locura y Poder

🎯 **Sistema de Quiz Interactivo**
- 5 preguntas por historia
- Puntuación en tiempo real
- Explicaciones detalladas
- Interfaz amigable

🎨 **Diseño Cinematográfico**
- Carrusel de imágenes rotativo
- Animaciones fluidas
- Tema oscuro épico
- Tipografía elegante (Playfair Display + Lato)
- Totalmente responsivo (móvil, tablet, PC)

🧭 **Navegación Intuitiva**
- Botones Siguiente/Atrás
- Botón "Volver a Inicio" en cada historia
- Indicadores de progreso
- Enrutamiento suave

## 🚀 Stack Tecnológico

### Frontend
- **React 19.2.1** - Framework UI
- **TypeScript 5.6.3** - Tipado estático
- **Tailwind CSS 4.1.14** - Estilos utilitarios
- **Wouter 3.3.5** - Enrutamiento cliente-side
- **Framer Motion 12.23.22** - Animaciones
- **Radix UI** - Componentes accesibles
- **Lucide React** - Iconografía

### Build & Dev
- **Vite 7.1.7** - Bundler ultra-rápido
- **PostCSS 8.4.47** - Procesamiento CSS
- **Prettier 3.6.2** - Formateador de código

### Backend (Minimal)
- **Express 4.21.2** - Servidor HTTP
- **Node.js** - Runtime

## 📦 Instalación

### Requisitos Previos
- Node.js 18+ 
- npm o pnpm

### Pasos de Instalación

```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/marathon_website.git
cd marathon_website

# 2. Instalar dependencias
npm install
# o
pnpm install

# 3. Iniciar servidor de desarrollo
npm run dev
# o
pnpm dev

# 4. Abrir en navegador
# Visita http://localhost:3000
```

## 🛠️ Scripts Disponibles

```bash
# Desarrollo
npm run dev              # Inicia servidor de desarrollo (puerto 3000)

# Producción
npm run build            # Compila TypeScript y Vite
npm run start            # Inicia servidor Express

# Utilidades
npm run check            # Verifica tipos TypeScript
npm run format           # Formatea código con Prettier
npm run preview          # Previsualiza build de producción
```

## 📁 Estructura del Proyecto

```
marathon_website/
├── client/
│   ├── src/
│   │   ├── pages/                    # Páginas principales
│   │   │   ├── StoriesHome.tsx       # Página de inicio
│   │   │   ├── StoryDetail.tsx       # Detalle de historia
│   │   │   └── NotFound.tsx          # Página 404
│   │   │
│   │   ├── components/               # Componentes reutilizables
│   │   │   ├── StoryPage.tsx         # Contenedor de historia
│   │   │   ├── QuizComponent.tsx     # Sistema de quiz
│   │   │   ├── StoriesGallery.tsx    # Galería de historias
│   │   │   ├── HeroCarousel.tsx      # Carrusel de imágenes
│   │   │   ├── NavigationBar.tsx     # Barra de navegación
│   │   │   └── ui/                   # Componentes Radix UI
│   │   │
│   │   ├── lib/
│   │   │   ├── historiesData.ts      # Datos de 10 historias
│   │   │   ├── images.ts             # URLs de imágenes CDN
│   │   │   └── utils.ts              # Utilidades
│   │   │
│   │   ├── hooks/                    # Custom React hooks
│   │   ├── contexts/                 # React contexts
│   │   ├── App.tsx                   # Componente raíz
│   │   ├── main.tsx                  # Punto de entrada
│   │   └── index.css                 # Estilos globales
│   │
│   ├── public/                       # Archivos estáticos
│   ├── index.html                    # HTML principal
│   └── vite.config.ts                # Configuración de Vite
│
├── server/
│   └── index.ts                      # Servidor Express
│
├── package.json                      # Dependencias
├── tsconfig.json                     # Configuración TypeScript
└── vite.config.ts                    # Configuración de build
```

## 🖼️ Imágenes y Recursos

### Ubicación de Imágenes
Las imágenes cinematográficas están alojadas en **CDN externo** (no en el repositorio):

```typescript
// client/src/lib/historiesData.ts
export const stories: Story[] = [
  {
    id: "marathon",
    heroImage: "https://cdn.example.com/marathon.jpg",  // CDN
    // ...
  },
  // ... más historias
];
```

### URLs de CDN
Las imágenes se cargan automáticamente desde las URLs configuradas en `historiesData.ts`. No es necesario descargarlas.

**Ventajas**:
- ✅ Repositorio más ligero
- ✅ Carga más rápida
- ✅ Actualizaciones sin clonar
- ✅ Sin límites de tamaño

## 🎨 Personalización

### Cambiar Colores
Edita `client/src/index.css`:
```css
:root {
  --primary: #f4d06f;  /* Cambiar color dorado */
}
```

### Cambiar Tipografía
Edita `client/index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=TuFuente:wght@400;700&display=swap" rel="stylesheet" />
```

### Agregar Nueva Historia
Edita `client/src/lib/historiesData.ts`:
```typescript
{
  id: "nueva-historia",
  title: "Mi Nueva Historia",
  year: "2024",
  location: "Mi Ubicación",
  heroImage: "https://cdn.example.com/imagen.jpg",
  description: "Descripción...",
  sections: [ /* ... */ ],
  quiz: [ /* ... */ ]
}
```

## 🔒 Seguridad

### Implementado
- ✅ HTTPS (en producción)
- ✅ Content Security Policy
- ✅ XSS Protection (React escapa automáticamente)
- ✅ Validación de entrada
- ✅ Headers de seguridad

### Recomendaciones
- Usar variables de entorno para datos sensibles
- Auditar dependencias regularmente: `npm audit`
- Mantener dependencias actualizadas
- Implementar rate limiting en producción

Ver `RECOMENDACIONES_SEGURIDAD.md` para más detalles.

## 📊 Rendimiento

- **Bundle Size**: ~150KB (gzipped)
- **Tiempo de Carga**: <2 segundos
- **Lighthouse Score**: 85+ (Performance)
- **Optimizaciones**: Code splitting, lazy loading, image optimization

## 🚢 Despliegue

### Opción 1: Manus (Recomendado)
```bash
# El proyecto está optimizado para Manus
# Usa el botón "Publish" en la interfaz de Manus
```

### Opción 2: Vercel
```bash
npm install -g vercel
vercel
```

### Opción 3: Netlify
```bash
npm install -g netlify-cli
netlify deploy
```

### Opción 4: GitHub Pages
```bash
# Modificar vite.config.ts
export default {
  base: '/marathon_website/',
  // ...
}

npm run build
# Subir carpeta dist/ a gh-pages
```

## 📚 Documentación Adicional

- **ANALISIS_TECNICO.md** - Análisis detallado de la arquitectura
- **GUIA_MODIFICACION_CODIGO.md** - Guía línea por línea para modificar código
- **RECOMENDACIONES_SEGURIDAD.md** - Mejores prácticas de seguridad

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama (`git checkout -b feature/AmazingFeature`)
3. Commit cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la licencia MIT. Ver `LICENSE` para más detalles.

## 👨‍💻 Autor

Creado con ❤️ usando React, TypeScript y Tailwind CSS.

## 🆘 Soporte

Si encuentras problemas:

1. Verifica que Node.js esté actualizado
2. Elimina `node_modules` y `package-lock.json`, luego ejecuta `npm install`
3. Revisa la consola del navegador (F12) para errores
4. Abre un issue en GitHub

## 🎯 Roadmap

- [ ] Agregar sistema de logros/badges
- [ ] Comparador de historias
- [ ] Modo claro/oscuro switchable
- [ ] Búsqueda y filtrado
- [ ] Compartir en redes sociales
- [ ] Exportar resultados de quiz
- [ ] Versión multiidioma

## 📞 Contacto

- GitHub: [@tu-usuario](https://github.com/tu-usuario)
- Email: tu-email@example.com

---

**Hecho con 🎬 Cinematografía Épica** ✨
