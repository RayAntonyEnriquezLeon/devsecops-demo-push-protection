# Demostración de GitHub Push Protection

Repositorio público de prueba con un README en la rama `main`. Se usó para verificar que el servidor de GitHub rechaza un push que coincide con un patrón admitido.

## Resultado observado

1. Con Push Protection activo, GitHub aceptó un cambio limpio.
2. GitHub aceptó una URL ficticia de PostgreSQL con los patrones genéricos deshabilitados. Se retiró la rama de esa prueba.
3. GitHub rechazó una cadena sintética con formato de token personal y devolvió `GH013`. Se verificó que la referencia remota nunca se creó. El código de salida del push fue 1 y `git ls-remote --exit-code` devolvió 2 para esa referencia.

Las pruebas usaron datos inertes preparados para el laboratorio. Las ejecuciones se conservaron como registros redactados.
