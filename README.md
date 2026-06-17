 📡 Torres y Antenas de Panamá

[![Estado del Proyecto](https://img.shields.io/badge/estado-activo-brightgreen.svg)](https://github.com/tu-usuario/torres-antenas-panama)
[![Licencia](https://img.shields.io/badge/licencia-MIT-blue.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/es/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
[![Leaflet](https://img.shields.io/badge/Leaflet-199900?logo=leaflet&logoColor=white)](https://leafletjs.com/)

> **Aplicación web interactiva** para visualizar la infraestructura de torres y antenas de telecomunicaciones en la República de Panamá.

![Vista previa del mapa](https://via.placeholder.com/800x400?text=Mapa+de+Torres+y+Antenas+de+Panamá)

## ✨ Características

- 🗺️ **Mapa interactivo** con OpenStreetMap como capa base
- 📍 **Visualización precisa** de todas las torres y antenas
- 🎯 **Filtro por provincia** para una navegación más específica
- 🎨 **Marcadores codificados por colores** según la altura de la estructura
- 📊 **Estadísticas en tiempo real** con distribución por provincia
- 💡 **Popups informativos** con todos los detalles de cada torre
- 📱 **Diseño responsive** adaptable a dispositivos móviles y tablets
- 🔄 **Actualización dinámica** sin recargar la página

## 🚀 Demo

Puedes ver una demostración en vivo aquí:  
[🔗 Ver Demo](https://tu-usuario.github.io/torres-antenas-panama)

## 📋 Requisitos

- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexión a internet (para cargar mapas de OpenStreetMap)
- Archivo `torres.geojson` con los datos de las torres

## 🛠️ Tecnologías Utilizadas

- **HTML5** - Estructura de la aplicación
- **CSS3** - Estilos y diseño responsive
- **JavaScript (ES6+)** - Lógica de la aplicación
- **Leaflet.js** - Biblioteca para mapas interactivos
- **OpenStreetMap** - Mapas base gratuitos
- **GeoJSON** - Formato de datos geoespaciales

## 📦 Estructura del Proyecto
torres-antenas-panama/
├── index.html # Archivo principal de la aplicación
├── torres.geojson # Datos geoespaciales de las torres
├── README.md # Documentación del proyecto
└── LICENSE # Licencia del proyecto (opcional)

text

## 📊 Formato del Archivo GeoJSON

El archivo `torres.geojson` debe contener las siguientes propiedades:

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `Operador` | String | Nombre del operador de telecomunicaciones |
| `Sitio Tran` | String | Nombre o identificación del sitio |
| `Estructura` | String | Tipo de estructura (torre, antena, etc.) |
| `Altura (m)` | Real | Altura en metros |
| `Lat_Dec` | Real | Latitud en grados decimales |
| `Lon_Dec` | Real | Longitud en grados decimales |
| `PROV_ID` | String | ID de la provincia |
| `PROV_NOMB` | String | Nombre de la provincia |
| `DIST_ID` | String | ID del distrito |
| `DIST_NOMB` | String | Nombre del distrito |
| `CORR_ID` | String | ID del corregimiento |
| `CORR_NOMB` | String | Nombre del corregimiento |

### Ejemplo de Feature en GeoJSON

```json
{
  "type": "Feature",
  "properties": {
    "Operador": "Cable & Wireless",
    "Sitio Tran": "Torre C&W - Panamá",
    "Estructura": "Torre autosoportada",
    "Altura (m)": 85,
    "Lat_Dec": 8.9823,
    "Lon_Dec": -79.5193,
    "PROV_ID": "1",
    "PROV_NOMB": "Panamá",
    "DIST_ID": "1",
    "DIST_NOMB": "Panamá",
    "CORR_ID": "1",
    "CORR_NOMB": "San Francisco"
  },
  "geometry": {
    "type": "Point",
    "coordinates": [-79.5193, 8.9823]
  }
}
🎯 Cómo Usar
Clonar el repositorio

bash
git clone https://github.com/tu-usuario/torres-antenas-panama.git
cd torres-antenas-panama
Colocar el archivo de datos

Copia tu archivo torres.geojson en la raíz del proyecto

Asegúrate de que tenga el formato correcto

Abrir la aplicación

Abre index.html en tu navegador

O usa un servidor local como Live Server en VS Code

Explorar el mapa

Navega por el mapa usando zoom y arrastre

Selecciona una provincia en el menú desplegable para filtrar

Haz clic en cualquier marcador para ver detalles

Usa los botones para limpiar filtros o ver estadísticas

🎨 Sistema de Colores
Los marcadores se codifican según la altura:

Color	Altura	Descripción
🟢 Verde	≤ 50 m	Torres de baja altura
🟠 Naranja	51 - 100 m	Torres de altura media
🔴 Rojo	> 100 m	Torres de gran altura
📈 Funcionalidades Destacadas
Filtro por Provincia
Lista desplegable con todas las provincias disponibles

Actualización automática del mapa al seleccionar una provincia

Contador dinámico mostrando el número de torres visibles

Estadísticas
Distribución de torres por provincia

Porcentajes calculados automáticamente

Información presentada en formato de alerta

Popups Informativos
Muestra todos los datos relevantes de cada torre

Información organizada y fácil de leer

Incluye datos de ubicación administrativa

🖥️ Personalización
Cambiar el Título
html
<!-- En index.html -->
<div class="header">
    <h1>📡 TORRES Y ANTENAS DE PANAMÁ</h1>
</div>
Modificar el Crédito
html
<!-- En index.html - footer -->
<div class="footer">
    Desarrollado por <span>Raul Viquez</span> | © 2026 Todos los derechos reservados
</div>
Ajustar Colores de Marcadores
javascript
// En index.html - función mostrarTorres()
let iconColor = '#00C853'; // Verde - baja
if (altura > 50) iconColor = '#FF6F00'; // Naranja - media
if (altura > 100) iconColor = '#D50000'; // Rojo - alta
Cambiar el Mapa Base
javascript
// Reemplazar OpenStreetMap con otro proveedor
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>'
}).addTo(map);
📱 Compatibilidad
Navegador	Versión	Soporte
Chrome	60+	✅ Completo
Firefox	55+	✅ Completo
Safari	12+	✅ Completo
Edge	79+	✅ Completo
Opera	47+	✅ Completo
iOS Safari	12+	✅ Completo
Android Chrome	60+	✅ Completo
🤝 Contribuciones
Las contribuciones son bienvenidas. Para contribuir:

Haz un Fork del proyecto

Crea tu rama de características (git checkout -b feature/AmazingFeature)

Haz commit de tus cambios (git commit -m 'Add some AmazingFeature')

Push a la rama (git push origin feature/AmazingFeature)

Abre un Pull Request

Reportar Problemas
Si encuentras algún problema, por favor abre un Issue con:

Descripción detallada del problema

Pasos para reproducirlo

Capturas de pantalla (si aplica)

Información del navegador

📄 Licencia
Este proyecto está bajo la Licencia MIT - ver el archivo LICENSE para más detalles.

👨‍💻 Autor
Raul Viquez

GitHub: @tu-usuario

LinkedIn: tu-linkedin

🙏 Agradecimientos
OpenStreetMap por los mapas base gratuitos

Leaflet.js por la excelente biblioteca de mapas

Todos los operadores de telecomunicaciones que proporcionan los datos

📊 Estado del Proyecto
✅ Activo - En desarrollo continuo
