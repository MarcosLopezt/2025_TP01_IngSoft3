# Decisiones del trabajo practico

## Configuración inicial

Configuré mi identidad global en Git:

- user.name = "Tu Nombre"
- user.email = "tuemail@ejemplo.com"
  Esto asegura trazabilidad en los commits.

## Estrategia de ramas

Cree la rama "development" desde main, para ordenar el trabajo que esta en desarrollo, entonces queda siempre
estable la rama main y en development se integran las funcionalidades en curso.

Cree la rama "feature/nueva-funcionalidad".
Las ramas features nacen desde development y se integran con las diferentes features que se crean
en development.

Luego la rama feature/nueva-funcionalidad la mergeamos con development, y development con main, asi quedan los cambios actualizados.

Hice 2 commits atómicos:

1. Agregar la función de validación (unidad de lógica independiente).
2. Integrar la validación en el flujo principal.
   Es buena practica hacer un commit para cada archivo o cada accion que se hace, para que sea facil revertir
   cambios y mantener trazabilidad.

## Simulacion de error

Modifique el archivo app.js en la rama main para simular el error, luego mergie main a development
para traer el error a la rama de desarrollo, de ahi cree una rama "fix/error-appjs".
Solucione el error en la rama creada, y luego la mergie a development, y development mergie a main
para tener el error corregido en la rama principal.

Utilice merge en vez de cherry-pick porque quiero mantener la historia completa de que se creo una
rama fix en development para corregir el error.

## Versionado

Cree el tag v1.0.0 para marcar la primera version estable.
Segui el esquema de versionado semantico porque es muy comun dentro de la industria del software.
vX.Y.Z
X --> Cambios grandes, incompatibles con versiones anteriores.
Y --> Cambios medianos, que son compatibles con versiones anteriores.
Z --> Correcciones menores o fixes que no afectan compatibilidad.
