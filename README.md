# Prueba Práctica — Unidad IV — Paralelo B

**Asignatura:** Ingeniería de Requisitos (ISR-401)
**Docente:** Ing. Gleiston Guerrero, Mg.
**Caso:** Sistema de Reserva de Citas Médicas

## Datos de identificación

- **Estudiante:** Genesis Adriana Gutierrez Ortega
- **Cédula:** 1250274477
- **Correo institucional:** ggutierrezo@uteq.edu.ec
- **Universidad:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Ciencias de la Computación — Carrera de Ingeniería de Software
- **Modalidad:** Individual, en clase
- **Fecha:** 12/08/2026

## Descripción

Este repositorio contiene el desarrollo de la Prueba Práctica de la Unidad IV, aplicada al caso Sistema de Reserva de Citas Médicas: una clínica que necesita gestionar la solicitud, confirmación, atención y cancelación de citas de sus pacientes según la disponibilidad de cupos en la agenda de cada médico.

Sobre este caso se desarrollaron las actividades P1 a P8: modelo de clases UML, diagrama de actividades, máquina de estados, verificación cruzada de consistencia entre los tres modelos, especificación de requisitos con esquema de atributos según ISO/IEC/IEEE 29148:2018, priorización MoSCoW, validación por inspección con checklist 29148 y pruebas de aceptación trazadas a los requisitos.

## Estructura del repositorio

Repositorio: `EVALUACION_U4_IR_GUTIERREZGENESIS_4toB`

```
.
├── 01_Cuestionario/
│   └── ...                                       # Evidencia del cuestionario rendido en el SGA
├── 02_Practica Citas Médicas/
│   ├── figuras/                                   # Imágenes de los diagramas UML (clases, actividades, estados)
│   ├── PE_U4_Practica_Citas_ParaleloB.tex          # Archivo principal en LaTeX
│   ├── PE_U4_Practica_Citas_ParaleloB.pdf          # PDF compilado de la prueba práctica
│   └── referencias.bib                             # Bibliografía (biblatex/biber)
├── .gitignore
├── EvaluacionPractica+Cuestionario_Gutierrez.pdf   # PDF con carátula, URL del repositorio y capturas del SGA (entregable al LMS)
└── README.md                                       # Este archivo
```

## Instrucciones de compilación

**Compilador:** `pdflatex` (motor LaTeX estándar), con `biber` para procesar la bibliografía.

**Archivo principal:** `02_Practica Citas Médicas/PE_U4_Practica_Citas_ParaleloB.tex`

**Dependencias:**
- Distribución LaTeX completa (TeX Live o MiKTeX)
- Paquete `biblatex` con backend `biber`
- Paquetes estándar: `graphicx`, `geometry`, `booktabs`, `array`, `hyperref`, `xcolor` (u otros equivalentes según el preámbulo del archivo `.tex`)

**Orden de comandos (desde la raíz del repositorio):**

```bash
cd "02_Practica Citas Médicas"
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
biber PE_U4_Practica_Citas_ParaleloB
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
```

Se ejecuta `pdflatex` tres veces (con `biber` en medio) para asegurar la correcta resolución de referencias cruzadas, numeración de tablas/figuras y la bibliografía.

### Compilación con `latexmk` (alternativa recomendada)

```bash
cd "02_Practica Citas Médicas"
latexmk -pdf -bibtex PE_U4_Practica_Citas_ParaleloB.tex
```

## Reproducibilidad

Al clonar este repositorio y ejecutar los comandos anteriores dentro de la carpeta `02_Practica Citas Médicas`, el archivo `PE_U4_Practica_Citas_ParaleloB.pdf` debe generarse de forma idéntica al PDF ya incluido en esa misma carpeta, y coincidir con el contenido de la prueba práctica (P1–P8) integrado en `EvaluacionPractica+Cuestionario_Gutierrez.pdf`.

```bash
git clone <URL_DEL_REPOSITORIO>
cd EVALUACION_U4_IR_GUTIERREZGENESIS_4toB
cd "02_Practica Citas Médicas"
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
biber PE_U4_Practica_Citas_ParaleloB
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
pdflatex PE_U4_Practica_Citas_ParaleloB.tex
```
