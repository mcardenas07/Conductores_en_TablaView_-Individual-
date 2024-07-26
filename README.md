# Conductores_en_TablaView_-Individual-
![EJECUCION](https://github.com/user-attachments/assets/59fbd40c-fd68-4aa3-9249-7ec70561a5a2)


### Paquetes e Importaciones

Se importan las clases necesarias de JavaFX para crear la interfaz gráfica y las clases modelo y repositorio del paquete `demo_jdbc`.

### Clase Principal

La clase principal `Main` extiende `Application` de JavaFX, permitiendo la creación de una aplicación JavaFX.

### Variables de Instancia

- `constructorResultRepository` y `seasonRepository` son instancias de repositorios para interactuar con los datos de la base de datos.
- `table` es una `TableView` que mostrará los resultados de los constructores.

### Método `start`

Este método se ejecuta al iniciar la aplicación JavaFX.

- Se configura el título de la ventana principal.

### ComboBox para Seleccionar Años

- Se crea un `ComboBox` para seleccionar el año.
- `getSeasons()` llena el `ComboBox` con los años disponibles obtenidos de la base de datos.
- Al seleccionar un año, se actualiza la `TableView` con los resultados de los constructores para ese año.

### Configuración de Columnas de la Tabla

- Se definen las columnas de la `TableView` para mostrar el nombre del constructor, victorias, puntos totales y rango.
- `PropertyValueFactory` se usa para enlazar cada columna con el atributo correspondiente del objeto `ConstructorResult`.

### Layout y Escena

- Se crea un `VBox` que contiene el `ComboBox` y la `TableView`.
- Se establece el espaciado y el relleno del `VBox`.
- Se crea una `Scene` con el `VBox` y se establece en la ventana principal (`primaryStage`).
- Se muestra la ventana principal (`primaryStage.show()`).

### Métodos Auxiliares

- `getSeasons()` obtiene la lista de años desde el `SeasonRepository` y la ordena en orden ascendente.
- `getConstructorResultsByYear(int year)` obtiene los resultados de los constructores para un año específico desde el `ConstructorResultRepository` y los convierte en una `ObservableList`.

### Método `main`

- `launch(args)` inicia la aplicación JavaFX.
