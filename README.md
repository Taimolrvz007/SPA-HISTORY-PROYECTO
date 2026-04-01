# Router SPA - Homework

## Autor
**Nombre:** josue salazar (taimolrvz)

---

## Descripción

SPA (Single Page Application) con routing del lado del cliente usando la History API. Implementa 3 vistas (Home, Chat, About) con navegación sin recarga, soporte de Back/Forward, render inicial correcto y manejo de rutas inexistentes (404).

---

## Estructura del proyecto

```
project/
├── index.html
├── styles.css
├── serve.json
├── README.md
└── src/
    ├── main.js
    ├── router.js
    ├── navigation.js
    └── views/
        ├── home.js
        ├── chat.js
        ├── about.js
        └── notFound.js
```

---

## Cómo correr el proyecto

```bash
npx serve .
```

Luego abrir en el navegador: `http://localhost:3000`

---

## Casos de prueba

### ✅ Test 1: Navegación interna sin recarga
- Abrir `/` (Home)
- Click en link a Chat
- La URL cambia a `/chat`, la vista cambia, sin recarga

### ✅ Test 2: Back/Forward funciona
- Navegar: Home → Chat → About
- Back → vuelve a Chat
- Back → vuelve a Home
- Forward → va a Chat
- URL y vista siempre sincronizadas

### ✅ Test 3: Deep link
- Abrir directamente `/about` en la URL
- Muestra la vista About correctamente sin pasar por Home

### ✅ Test 4: Ruta inexistente (404)
- Navegar a `/nonexistent`
- Muestra vista 404 con mensaje de error
- Link "Volver al inicio" funciona

### ✅ Test 5: Ctrl+click abre nueva pestaña
- Ctrl+click en link interno
- Se abre en nueva pestaña, la pestaña original no navega

### ✅ Test 6: Links externos no se interceptan
- Click en link externo (Google)
- Navega a Google sin interceptarse

---

