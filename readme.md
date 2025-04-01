# Releases

La idea de este repositorio es subir las releases públicas que se compilen. En general son las últimas que se buildean para entrega de clientes. Las relacionadas a testeos quedan guardadas en los repositorios privados.

[ver releases](./releases.md)

## ¿Cómo subir una release en este repositorio?

### 1) Crear un nuevo item en `relases.md`

Ese item debe contener la versión y la fecha de publicación.

Ejemplo:

```
v0.1.1: 2025-03-31T02:18:19Z
```

### 2) Detalle nuevo release

En la carpeta releases crear un nuevo archivo `.md` en donde se debería detallar lo que incluye el nuevo release (se puede sacar de la release privada del repositorio correspondiente)

[Acá un ejemplo](./releases/agenda-quirofano/v0.1.1.md)

### 3) Commit

Crear un commit con `git commit -am "<app>/v<version>: <message>`.

Ejemplo:

```
git commit -am "agenda-quirofano/v0.1.1: Crea release de nueva versión necesaria para..."
```

### 4) Creación de etiqueta (<i>tag</i>)

Crear una tag localmente más un mensaje con `git tag -a <app>/v<version> -m "<description>"`.

Ejemplo:

```
git tag -a agenda-quirofano/v0.1.1 -m "Agenda de Quirófano, versión 0.1.1"
```

### 5) Push del commit + tag al repositorio remoto

Pushear esa tag al repositorio con

```
git push origin main --follow-tags
```

### 6) Crear el release de la nueva tag y adjuntar binarios

Una vez ubicada la nueva etiqueta en el repositorio de github, se debe crear un release con esa etiqueta y se debe adjuntar los binarios correpondientes
