---
name: ui-ux-hyperpolished
description: Instrucciones estrictas para la creación de UI/UX minimalista, realista y con animaciones fluidas basados en física. Usa cuando se pidan componentes UI, vistas o animaciones.
---

# Reglas de Diseño UI/UX y Animación Realista

## 1. Animaciones y Movimiento
- NUNCA uses `transition: all 0.3s ease` o transiciones genéricas simples.
- Usa prioritariamente **Framer Motion** con físicas de muelle (*spring*):
  - `type: "spring"`, `stiffness: 300`, `damping: 30`.
- Aplica `staggerChildren` para elementos repetidos (listas, grillas, cards).
- Micro-interacciones obligatorias en botones y elementos interactivos:
  - Hover: escala sutil (`scale: 1.02`), elevación de sombra.
  - Tap/Click: respuesta física (`scale: 0.98`).

## 2. Estética y Visual (Realista y Minimalista)
- **Profundidad Realista:** Usa capas de sombra compuestas en CSS o Tailwind, no sombras planas directas.
- **Tipografía:** Evita fuentes genéricas sobreusadas como Inter o Roboto salvo que se especifique. Prefiere tipografías editoriales/modernas con alto contraste de jerarquía.
- **Glassmorphism y Bordes:** Utiliza bordes sutiles `border border-white/10` o `border-black/5` combinados con `backdrop-blur-md`.
- **Estructura Bento Box:** Prioriza tarjetas de esquinas suavizadas (`rounded-2xl`), espaciado uniforme y distribución limpia del contenido.

## 3. Código y Rendimiento
- Garantiza accesibilidad (`aria-*`, contraste de color mínimo 4.5:1).
- Limita repeticiones de renderizado usando componentes modulares limpios.
