# Decisiones

Cree la rama "development" desde main, para ordenar el trabajo que esta en desarrollo, entonces queda siempre
estable la rama main y en development se integran las funcionalidades en curso.

Cree la rama "feature/nueva-funcionalidad".
Las ramas features nacen desde development y se integran con las diferentes features que se crean
en development.

Hice 2 commits atómicos:

1. Agregar la función de validación (unidad de lógica independiente).
2. Integrar la validación en el flujo principal.
   Es buena practica hacer un commit para cada archivo o cada accion que se hace, para que sea facil revertir
   cambios y mantener trazabilidad.
