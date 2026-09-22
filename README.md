# Taller Integrador: Cortes 1 y 2 - Buenas Prácticas de Desarrollo de Software
**Estudiante:** Mario Andree Rivera Altamar  
**Institución:** Universidad de la Costa (CUC)  
**Asignatura:** Buenas Prácticas de Desarrollo de Software  

---

## Enlace al Sitio Publicado
- **Netlify:** https://zingy-kataifi-ba3f90.netlify.app
---

## Tabla de Hallazgos de la Auditoría

| Defecto encontrado | Por qué era un problema | Cómo lo corrigió |
| :--- | :--- | :--- |
| Nombres de archivo con mayúsculas y espacios (`Mi Pagina De Notas.HTML` y `Estilos Del Sitio.CSS`) | Rompe los estándares de nomenclatura web y genera errores de resolución de rutas en servidores Linux y Netlify. | Se renombraron a `index.html` y `styles.css`. |
| Título genérico en la pestaña del navegador (`<title>Document</title>`) | No comunica el propósito del aplicativo al usuario ni aporta a la accesibilidad del sitio. | Se cambió por `<title>Calculadora de Promedio de Notas</title>`. |
| Variables globales y de nombres crípticos (`TempValue2`, `x`, `a`, `b`, `c`) | No expresan qué dato almacenan y dificultan la lectura y el mantenimiento del código. | Se renombraron a variables descriptivas en camelCase (`nota1`, `nota2`, `nota3`, `promedio`) y se definió la constante `CANTIDAD_NOTAS`. |
| Nombre de función ambiguo (`calc()`) | Es un nombre genérico que no explicita la acción ni la responsabilidad de la función. | Se renombró a `calcularPromedio()`. |
| Identificadores HTML poco semánticos (`id="n1"`, `id="n2"`, `id="n3"`, `id="r"`, `id="r2"`) | Complican la legibilidad de la estructura y la vinculación lógica entre el DOM, JavaScript y CSS. | Se actualizaron a IDs semánticos: `id="nota-1"`, `id="nota-2"`, `id="nota-3"`, `id="texto-promedio"`, `id="estado-aprobacion"` y `id="btn-calcular"`. |
| Líneas de código muerto y registros residuales de depuración | Generan deuda técnica y sobrecargan la consola del navegador innecesariamente. | Se eliminaron las sentencias huérfanas y los llamados a `console.log(...)`. |
| Ausencia de restricciones numéricas completas en los campos de entrada | Permite el ingreso de valores por fuera de la escala real de calificación académica. | Se agregaron los atributos `min="0"`, `max="5"` y `step="0.1"` a cada input de notas. |
| Formato e indentación inconsistente en los bloques de código | Dificulta la lectura jerárquica del marcado HTML y las reglas CSS. | Se ordenó la estructura aplicando un espaciado uniforme a todo el proyecto. |