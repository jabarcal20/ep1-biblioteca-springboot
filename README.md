# Ep1-Biblioteca-Springboot
## 1. Convención de Commits

- Durante el desarrollo del proyecto no se utilizó una convención formal
como Conventional Commits.

- Los mensajes de commit se utilizaron para describir de manera breve
los cambios realizados en cada modificación del proyecto.

## 2. Ramas y Flujo de Trabajo

- Utilizamos Trunk-Based Development, trabajando principalmente sobre
la rama `main`.

- Los cambios se prueban localmente antes de realizar el commit y
posteriormente se integran directamente a `main`.


# 3. Integración Continua y Revisión
- **GitHub Actions:** Cada vez que hacemos `git push origin main`, se activa automáticamente el pipeline de CI para verificar que el proyecto siga compilando.
- **Revisión de cambios:** Antes de dar por terminado un ajuste, revisamos que los microservicios levanten en su orden (Eureka -> Usuarios -> Catálogo -> Recursos -> Gateway) y que no se rompan las dependencias en el `pom.xml`.
