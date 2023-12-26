
# Extracción de Datos de Certificados de Propiedad con Computer Vision y AWS Textract

Este proyecto se enfoca en la extracción precisa de información clave de certificados de propiedad inmobiliaria colombianos. Se proporcionan dos archivos PDF correspondientes a certificados de propiedad, junto con archivos JSON generados por AWS Textract. Estos archivos JSON contienen datos extraídos de la primera página de cada PDF, incluyendo texto y coordenadas.

## Contenido del Repositorio

- `II.Computer Vision.ipynb`: Archivo Jupyter Notebook que contiene el código en Python para la extracción de datos.
- `files/`: Carpeta que incluye los archivos PDF y sus archivos JSON asociados.

## Requisitos Previos

Es necesario tener instaladas las siguientes bibliotecas de Python:

- `textract-trp`
- `PyMuPDF`
- `Pillow`
- `opencv-python`

## Instrucciones de Uso

1. **Entorno de Ejecución:** El código está configurado para ejecutarse en Google Colab.
2. **Montaje de Google Drive:** Se utiliza para acceder a los archivos. Asegúrate de modificar las rutas de archivos (`json_001_pag1`, `json_041_pag1`, etc.) según la ubicación en tu Google Drive.
3. **Extracción de Datos:** El código extrae los siguientes campos de los certificados:
   - Número de Matrícula
   - Fecha de Impresión (en formato AAAA-MM-DD)
   - Departamento
   - Municipio
   - Localidad (Vereda)
   - Estado del Folio

## Funcionalidades del Código

El código Python se organiza en secciones que cumplen diversas funciones:

- Carga de archivos JSON y su procesamiento con `trp` para representar la estructura de datos.
- Utilización de expresiones regulares para extraer información específica de los certificados.
- Conversión de páginas de PDF a imágenes para visualizar áreas donde se encontró la información extraída.

## Uso con Otros Certificados

Para emplear este código con certificados diferentes pero con una estructura similar, se deben proporcionar los archivos PDF correspondientes y sus archivos JSON asociados en la carpeta `files/`. Asegúrate de ajustar las rutas de los archivos en el código según sea necesario para trabajar con los nuevos archivos.

## Notas Adicionales

- Si la estructura o disposición de los campos en los certificados varía significativamente, el código puede necesitar modificaciones.
- Puede adaptarse para trabajar con múltiples páginas o documentos PDF distintos.
- Asegúrate de realizar ajustes si los certificados difieren en formatos de fechas, nombres de campos, etc.

---

