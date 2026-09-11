# ep1-biblioteca-springboot
# Commits en git
# 1. Convención de Commits (Conventional Commits)
Para mantener el historial ordenado y saber qué hizo cada uno, usamos estos prefijos:

- **`feat:`**: Para agregar cosas nuevas, plantillas o documentación.
  - *Ejemplos de lo que se subió al proyecto:*
    - `feat: add environment variables template for microservices`
    - `feat: add microservices port reference documentation`
- **`fix:`**: Para corregir errores de código, scripts o configuraciones que fallaban.
  - *Ejemplo*
    - `fix: update db script header compatibility`
- **`docs:`**: Para actualizar el README o guías del proyecto.

# 2. Ramas y Flujo de Trabajo
- **`main`**: Es la rama principal y la fuente de verdad. Todo cambio se sube aquí de forma continua.
- **Ramas cortas:** Si hay que probar un arreglo de un microservicio sin romper lo de los demás, creamos una rama temporal

# 3. Integración Continua y Revisión
- **GitHub Actions:** Cada vez que hacemos `git push origin main`, se activa automáticamente el pipeline de CI para verificar que el proyecto siga compilando.
- **Revisión de cambios:** Antes de dar por terminado un ajuste, revisamos que los microservicios levanten en su orden (Eureka -> Usuarios -> Catálogo -> Recursos -> Gateway) y que no se rompan las dependencias en el `pom.xml`.