# LEC Tool: Cálculo de curvas de excedencia de pérdidas y evaluación de estrategias de gestión de riesgo
La herramienta **LEC Tool** consiste en una plataforma desarrollada por el **Banco Interamericano de Desarrollo** con el propósito de derivar curvas de excedencia de pérdidas (LEC) a partir de registros históricos de desastres. Esta plataforma está diseñada para estimar la tasa de excedencia anual asociada a valores específicos de pérdidas económicas. La curva LEC resultante se utiliza posteriormente en análisis de riesgo y en la toma de decisiones para la gestión de desastres, particularmente para la selección de estrategias de transferencia y/o reducción de riesgo.

![version](https://img.shields.io/badge/version-0.1.0-blue)

# ✨ Descripción

La LEC Tool está programada a partir de un set de scripts en Python desarrollados por el equipo de Gestión de Riesgos de Desastres del Banco Interamericano de Desarrollo. La aplicación cuenta con un grupo de módulos secuenciales:

-	Pantalla de Inicio 
-	Entrada LEC (Input de datos de pérdidas)
-	Curva LEC (Resultados de curva de excedencia de pérdidas)
-	Catálogo Sintético (Simulación de perdidas futuras)
-	Gestión del Riesgo (Evaluación de mecanismos de transferencia y reducción de riesgo)

# 📄 Guía de Usuario
La herramienta presenta una barra de navegación con acceso secuencial, a excepción de la última pestaña, que contiene las instrucciones y documentación para el uso de la aplicación.

## 📄1️⃣Pantalla inicial

En la pantalla inicial se dispone de:

* **Iniciar nueva corrida:** Un botón para comenzar un nuevo proceso desde cero. Al hacerlo, el sistema generará automáticamente un nuevo **AnalysisId**. Este identificador único es generado automáticamente por el sistema y define la semilla aleatoria de los análisis para poder recuperar sus análisis en el futuro. 
* **Visualizar corrida previa:** Un campo de entrada (*input*) donde el usuario deberá ingresar el **AnalysisId** correspondiente a una ejecución anterior para consultarla.

## 📄2️⃣Entrada LEC

En esta sección, el usuario podrá cargar los archivos de entrada necesarios para el procesamiento de la herramienta:

1.  **Archivo de Curva LEC (.csv):** Utilizado para graficar la curva LEC.
2.  **Archivo de Eventos y Pérdidas (.csv):** Requerido para el cálculo de estadísticas y la generación de la matriz de pérdidas agregadas por año. *Nota: Si no se dispone de un archivo de curva LEC, este archivo será empleado para generarla.*

### Configuración adicional

* **Responsabilidad fiscal del Estado:** Se debe ingresar un porcentaje (valor entre 0 y 100). Este dato se utiliza para calcular y visualizar indicadores como la retención fiscal.
* **Desglose (Opcional):** El usuario puede completar un desglose ilustrativo que detalle la distribución de dicha responsabilidad fiscal entre distintos sectores del Estado.

### Supuestos de la corrida

Se incluyen los datos identificatorios del proceso:
* **Responsable:** Persona a cargo de la ejecución.
* **Fecha:** Fecha de registro o ejecución.
* **País:** País asociado a la corrida.
* **AnalysisId:** Campo autocompletado generado por la herramienta.

> Una vez cargados los archivos y completados los campos, haga clic en **“Procesar datos y visualizar curva LEC”** para avanzar.

## 📄3️⃣Curva LEC

Esta pantalla tiene un propósito principalmente visual e informativo. En ella se presentan:

* El gráfico de pérdidas agregadas por año.
* Las estadísticas derivadas de dichas pérdidas.
* El gráfico de la curva LEC.

### Opciones de visualización
El gráfico de la Curva LEC dispone de cuatro tipos de escala:
* Escala natural
* Escala logarítmica en eje X
* Escala logarítmica en eje Y
* Escala logarítmica en ambos ejes

*El usuario puede descargar el archivo de la curva LEC mediante el enlace disponible debajo del botón de navegación.*

> Para continuar, seleccione **“Derivar catálogos de pérdidas sintéticos”**.

## 📄4️⃣ Catálogo Sintético

En esta etapa, el usuario debe especificar los parámetros para la simulación:

* **Número de simulaciones:** Cantidad total de catálogos a generar (valor entre 1 y 1000).
* **Horizonte de simulación (años):** Duración temporal de cada simulación (valor entre 5 y 15 años).

Al hacer clic en **“Generar catálogos”**, la herramienta procesará la información permitiendo:
1.  Visualizar cualquier catálogo individual junto con sus estadísticas.
2.  Consultar un gráfico resumen de todos los catálogos con sus indicadores.

*El archivo generado podrá descargarse mediante el enlace de descarga disponible debajo del botón de avance.*

> Para continuar, haga clic en **“Definir estrategias de gestión del riesgo”**.

## 📄5️⃣ Gestión del riesgo

En esta pantalla se pueden crear y visualizar estrategias compuestas por distintos mecanismos.

### Mecanismos disponibles

**De Cobertura (con parámetros configurables):**
* Seguros
* CCF
* PPO
* DDO

**De Reducción:**
* Perfil de inversión en reducción (configurable mediante parámetros específicos).

### Visualización de resultados
El usuario puede:
* Seleccionar el catálogo a visualizar.
* Consultar las estadísticas de gestión del riesgo.
* Representar gráficamente cualquiera de ellas.
* Ver un gráfico comparativo entre las distintas estrategias generadas.

*El resultado puede descargarse mediante el enlace disponible al pie de la pantalla.*

> Para finalizar o avanzar a la siguiente etapa, seleccione **“Elaborar informe de resultados”**.

# 🧑‍🍳 Autores

El motor y la metodología de cálculo del LEC Tool es desarrollado por el **Disaster Risk Management Team** del **Banco Interamericano de Desarrollo**. La plataforma informática es desarrollada y mantenida por [GreenCode Software](https://www.greencodesoftware.com/).

Equipo de desarrolladores:
Andrés Abarca, Kenneth Otárola, Ginés Suárez

# 📑 Licencia

Copyright© 2025. Banco Interamericano de Desarrollo ("BID"). Uso autorizado [AM-331-A3](https://github.com/andresabarca-atlas/BID-LECTool/edit/main/LICENSE.md)

## Limitación de responsabilidades

El BID no será responsable, bajo circunstancia alguna, de daño ni indemnización, moral o patrimonial; directo o indirecto; accesorio o especial; o por vía de consecuencia, previsto o imprevisto, que pudiese surgir:

i. Bajo cualquier teoría de responsabilidad, ya sea por contrato, infracción de derechos de propiedad intelectual, negligencia o bajo cualquier otra teoría; y/o

ii. A raíz del uso de la Herramienta Digital, incluyendo, pero sin limitación de potenciales defectos en la Herramienta Digital, o la pérdida o inexactitud de los datos de cualquier tipo. Lo anterior incluye los gastos o daños asociados a fallas de comunicación y/o fallas de funcionamiento de computadoras, vinculados con la utilización de la Herramienta Digital.
