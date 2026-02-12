# Plantilla de CV en LaTeX

Una plantilla profesional y limpia para crear currículums en formato PDF utilizando LaTeX, optimizada para sistemas de seguimiento de candidatos (ATS-friendly).
Pensada para tener al mismo tiempo una version digital y, si se necesita, impresa, del mismo CV.

- [Estructura de Archivos](#estructura-de-archivos)
- [Paquetes Requeridos](#paquetes-requeridos)
- [Personalización y Uso](#personalización-y-uso)
- [Comandos Disponibles](#comandos-disponibles)
- [Consejos](#consejos)
- [Notas](#notas)

## Estructura de Archivos

```
├── cv.tex          # Plantilla principal del CV. Este es el archivo a modificar principalmente.
├── config.tex      # Configuraciones y comandos personalizados. Edita aquí lo que consideres.
```

## Paquetes Requeridos

Esta plantilla utiliza los siguientes paquetes de LaTeX:

- `fullpage` - Configuración de márgenes mínimos
- `titlesec` - Personalización de formato de títulos de secciones
- `marvosym` - Símbolos adicionales (teléfono, email, etc.)
- `hyperref` - Hipervínculos en el documento (configurado con hidelinks)
- `enumitem` - Personalización de listas (itemize, enumerate)
- `fancyhdr` - Encabezados y pies de página personalizados
- `babel` - Soporte multiidioma (configurado para inglés y español.)
- `tabularx` - Tablas con ancho ajustable automáticamente
- `fontawesome5` - Íconos de redes sociales (GitHub, LinkedIn, etc.)
- `multicol` - Soporte para múltiples columnas
- `roboto` - Fuente sans-serif Roboto

Estos paquetes están generalmente incluidos en distribuciones completas de LaTeX como TeX Live o están preinstalados en [Overleaf](https://www.overleaf.com/).

## Personalización y Uso

### Editar tus datos

Abre el archivo `cv.tex` y reemplaza la información de ejemplo con tus datos personales:

1. **Encabezado**: Nombre completo, teléfono, correo, LinkedIn, GitHub
2. **Resumen Profesional**: Párrafo breve que resuma tu perfil
3. **Habilidades**: Lenguajes de programación, frameworks, bases de datos, idiomas, habilidades blandas
4. **Educación**: Títulos académicos
5. **Proyectos**: Proyectos personales o académicos (opcional)
6. **Experiencia Profesional**: Historial laboral
7. **Actividades Extracurriculares**: Voluntariado, comunidades tech (opcional)
8. **Certificaciones**: Credenciales y certificaciones profesionales

### Cambiar la fuente

Por defecto usa Roboto (sans-serif). Para cambiar, modifica esta línea en `config.tex`:

```latex
\usepackage[sfdefault]{roboto}  % Fuente actual
```

Otras opciones pueden requerir instalaciones de paquetes extra.

### Ajustar márgenes

En `config.tex`, modifica:

```latex
\addtolength{\oddsidemargin}{-0.6in}    % Margen izquierdo
\addtolength{\textwidth}{1.2in}         % Ancho del texto
\addtolength{\topmargin}{-.6in}         % Margen superior
\addtolength{\textheight}{1.0in}        % Altura del texto
```

## Comandos Disponibles

La plantilla define comandos personalizados en `config.tex`:

### `\cvItem{texto}`

Crea un ítem individual en listas.

**Uso:**
```latex
\cvItem{\textbf{Lenguajes}: Python, Java, JavaScript}
```

### `\cvSubtitulo{título}{fecha}{subtítulo}{ubicación}`

Crea un subencabezado para experiencia, educación o proyectos.

**Parámetros:**
- `título`: Nombre del puesto, institución o proyecto (en negrita)
- `fecha`: Período o fecha (alineada a la derecha)
- `subtítulo`: Empresa, universidad o descripción (en cursiva)
- `ubicación`: Ciudad, país o tecnologías (en cursiva, alineada a la derecha)

**Uso:**
```latex
\cvSubtitulo
  {Ingeniero de Software}{Enero 2020 - Presente}
  {Empresa XYZ}{Ciudad, País}
```

### `\ListaSubtitulo` y `\ListaSubtituloFin`

Inicia y cierra listas de subsecciones.

**Uso:**
```latex
\ListaSubtitulo
  \cvItem{\textbullet\ Primer logro}
  \cvItem{\textbullet\ Segundo logro}
\ListaSubtituloFin
```

## Consejos

1. **Longitud**: Mantén tu CV en 1-2 páginas máximo
2. **Verbos de acción**: Usa verbos fuertes al inicio de cada bullet point (Desarrollé, Implementé, Lideré, Optimicé, Diseñé, Automaticé)
3. **Cuantifica**: Siempre que sea posible, incluye números
   - "Mejoré el rendimiento en un 40%"
   - "Gestioné un equipo de 5 personas"
   - "Reduje costos en $10,000 anuales"
4. **Personaliza**: Ajusta tu CV para cada solicitud de trabajo, destacando las habilidades y experiencias más relevantes para el puesto
5. **ATS-friendly**: Usa palabras clave del anuncio de trabajo para que tu CV pase los sistemas automatizados de selección
6. **Revisa**: Verifica ortografía y gramática. Un error puede descalificarte
7. **Formato**: Mantén un formato consistente (fechas, mayúsculas, puntos)

## Notas
- Esta plantilla ha sido probada y funciona correctamente en [Overleaf](https://www.overleaf.com/).
- Si quieres ver un ejemplo completo de esta plantilla, puedes revisar [este link](https://wallsified.is-a.dev/documents/CV_DanielParedes.pdf).

## Copyright y Licencia de Uso
- El código original del este repo es obra de [@wallsified](https://wallsified.is-a.dev/), pero cualquier modificación posterior a este repo es por y pertenece a la comunidad [Sudo FCiencias](https://linktr.ee/sudo_FCiencias).
- La licencia de este repositorio se encuentra en una de las pestañas del repositorio.
