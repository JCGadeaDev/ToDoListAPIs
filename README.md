# 📝 ToDo List App

Una aplicación web moderna de lista de tareas que permite gestionar tareas de manera eficiente, con una arquitectura modular y sincronización en tiempo real mediante una API REST.

---

## 🚀 Características

- ✅ Crear nuevas tareas  
- 📝 Editar tareas existentes en tiempo real  
- ❌ Eliminar tareas  
- 📱 Interfaz responsiva y minimalista  
- 🔄 Sincronización con backend mediante [JSONPlaceholder API](https://jsonplaceholder.typicode.com)

---

## 🛠️ Tecnologías Utilizadas

- HTML5  
- CSS3  
- JavaScript (ES6+)  
- Módulos ES6  
- Fetch API  
- JSONPlaceholder API

---

## 📦 Estructura del Proyecto

```
ToDo-List/
├── index.html          # Archivo principal HTML
├── style.css           # Estilos de la interfaz
├── headers.json        # Configuración de cabeceras
└── lib/
    ├── index.js        # Controlador principal de la app
    ├── request.js      # Manejador de peticiones HTTP
    └── Todo.js         # Clase modelo para tareas
```

---

## 💻 Instalación y Uso

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/ToDo-List-App.git
   ```
2. Abre `index.html` en un servidor web local (por ejemplo, con la extensión **Live Server** de VS Code).
3. ¡Listo para usar!

---

## 🔍 Características Detalladas

### 📦 Clase `Todo`

```js
class Todo {
  static async all() {
    // Obtiene todas las tareas
  }

  constructor(args) {
    this.userId = args.userId;
    this.title = args.title;
    this.completed = args.completed;
    this.id = args.id;
  }

  save = async () => {
    // Crea o actualiza una tarea según si tiene ID
  }

  create = async () => {
    // Lógica para crear una nueva tarea
  }

  update = async () => {
    // Lógica para actualizar una tarea existente
  }

  destroy = async () => {
    // Lógica para eliminar la tarea
  }
}
```

---

### ⚙️ Sistema de Peticiones

- Arquitectura modular en `lib/request.js`  
- Métodos soportados: `GET`, `POST`, `PUT`, `DELETE`  
- Configuración de cabeceras en `headers.json`  
- Todas las operaciones interactúan con la API REST pública: [JSONPlaceholder](https://jsonplaceholder.typicode.com)

---

### 📱 Interfaz de Usuario

- Formulario para agregar nuevas tareas  
- Lista de tareas con edición directa (in-place)  
- Botones de eliminación intuitivos  
- Feedback visual inmediato al interactuar  
- Diseño responsivo para todo tipo de dispositivos

---

### 🎨 Estilos y Diseño

- Estética minimalista y limpia  
- Sombra suave para jerarquía visual  
- Tipografía Roboto para mejor legibilidad  
- Animaciones sutiles para mejorar la experiencia de usuario

---

## 🔄 API Endpoints Utilizados

```js
const endpoint = "https://jsonplaceholder.typicode.com";
```

| Método | Endpoint         | Descripción               |
|--------|------------------|---------------------------|
| GET    | `/todos`         | Obtener todas las tareas  |
| POST   | `/todos`         | Crear nueva tarea         |
| PUT    | `/todos/:id`     | Actualizar tarea existente|
| DELETE | `/todos/:id`     | Eliminar tarea            |

---

## ⚙️ Funcionalidades de Código

### Crear una tarea
```js
todo.save().then(() => {
  // Actualización de la UI
});
```

### Editar una tarea
```js
editInPlace(node, todo);
```

### Eliminar una tarea
```js
todo.destroy();
```

---

## 🤝 Contribución

Las contribuciones son bienvenidas.  
Si deseas mejorar este proyecto, por favor abre primero un *issue* para discutir los cambios propuestos antes de enviar un *pull request*.

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT.  
Consulta el archivo `LICENSE` para más detalles.

---

**Desarrollado como parte del curso de consumo de APIs con JavaScript (`fetch`) de [Código Facilito](https://codigofacilito.com).**
