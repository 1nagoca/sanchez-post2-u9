# PostContenido 2 - Unidad 9

## Seguridad Avanzada en Aplicaciones Web con Spring Security

### Autor

Camilo Sánchez

## Descripción del Proyecto

Este proyecto corresponde al PostContenido 2 de la Unidad 9 de Programación Web.

El objetivo principal fue fortalecer la seguridad de la aplicación desarrollada en el PostContenido 1 mediante la implementación y verificación de mecanismos avanzados de protección proporcionados por Spring Security y Thymeleaf.

Las funcionalidades implementadas incluyen:

* Autorización a nivel de método mediante `@PreAuthorize`.
* Página personalizada para errores 403 (Acceso Denegado).
* Mitigación de ataques XSS utilizando Thymeleaf.
* Configuración de Content Security Policy (CSP).
* Verificación de protección CSRF.
* Restricciones de acceso basadas en roles ADMIN y USER.

---

# Arquitectura de Seguridad

```text
Usuario
   |
   v
Spring Security
   |
   +--------------------+
   |                    |
   v                    v
@PreAuthorize      CSRF Protection
   |
   v
UsuarioService
   |
   v
Repository
   |
   v
MySQL

   ^
   |
Thymeleaf
   |
   +---- Mitigación XSS
   |
   +---- Vista Error 403

   ^
   |
CSP Header
```

---

# Estructura del Proyecto

```text
src
├── controller
├── service
├── repository
├── model
├── config
├── templates
│   ├── dashboard.html
│   ├── login.html
│   ├── registro.html
│   └── error
│       └── 403.html
└── application.properties
```
---

# Conclusiones

Se fortaleció la seguridad de la aplicación mediante controles de autorización a nivel de método utilizando `@PreAuthorize`, mitigación de ataques XSS mediante Thymeleaf, políticas Content Security Policy y protección CSRF proporcionada por Spring Security. Las pruebas realizadas demuestran que los mecanismos de seguridad funcionan correctamente y cumplen los requisitos establecidos para la actividad.
