# Test de Hipótesis y Chi-cuadrado en R

Material didáctico sobre **estadística inferencial aplicada a ciencia política**, usando R y datos reales de la Encuesta CEP N° 81 (septiembre-octubre 2017).

## 📋 Descripción

Este repositorio contiene un tutorial paso a paso para aplicar dos herramientas fundamentales de la estadística inferencial:

- **Test de hipótesis para una muestra** (media y proporción)
- **Test de Chi-cuadrado de independencia**

Ambas técnicas permiten pasar de la descripción de los datos a afirmaciones con respaldo estadístico sobre la población, algo clave en el análisis político empírico.

## 🎯 Contenidos

1. Introducción al test de hipótesis (H₀ vs H₁, p-valor, regla de decisión)
2. Test t para una media con `t.test()`
3. Test para una proporción con `prop.test()`
4. Test de Chi-cuadrado de independencia con `chisq.test()`
5. Ejercicios prácticos resueltos

## 📊 Datos

Se trabaja con la **Encuesta Nacional de Opinión Pública CEP N° 81** (septiembre-octubre 2017), aplicada pocas semanas antes de la primera vuelta presidencial de 2017.

Variables utilizadas:

| Variable | Descripción |
|----------|-------------|
| `EDAD_REC` | Edad del/la entrevistado/a en tramos |
| `SEXO` | 1 = Hombre, 2 = Mujer |
| `DPP_11` | Autoubicación política (0 = izquierda, 10 = derecha) |
| `MEP_4` | Intención de voto presidencial |

🔗 La base se puede descargar desde el sitio oficial del [Centro de Estudios Públicos](https://www.cepchile.cl/).

## 🛠️ Requisitos

- **R** (versión 4.0 o superior recomendada)
- **RStudio** (opcional pero recomendado)

Paquetes necesarios:

```r
install.packages(c("haven", "dplyr", "ggplot2"))
```

## 🚀 Cómo usar este material

1. Clona o descarga este repositorio
2. Descarga la base de la CEP N° 81 en formato `.sav`
3. Coloca el archivo en tu directorio de trabajo
4. Abre el script en RStudio y ejecuta los bloques en orden

```r
library(haven)
library(dplyr)
library(ggplot2)

cep <- read_sav("Encuesta CEP 81 Sep-Oct 2017 v1.sav")
```

## Ejercicios propuestos

El material incluye cuatro ejercicios para practicar:

1. Test de media sobre autoubicación ideológica
2. Test de proporción sobre aprobación de gestión presidencial
3. Chi-cuadrado entre sexo e intención de voto
4. Reflexión sobre interpretación del p-valor

##  Resumen de funciones

| Situación | Hipótesis nula | Función en R |
|-----------|----------------|--------------|
| Testear una media | μ = μ₀ | `t.test(x, mu = μ₀)` |
| Testear una proporción | p = p₀ | `prop.test(x, n, p = p₀)` |
| Asociación entre variables categóricas | Independencia | `chisq.test(tabla)` |

##  Autoría

Material elaborado por **Francisca Hernández**
franhc123@gmail.com

Desarrollo propio en base a contenidos del curso, complementado con recursos disponibles en internet.

## Licencia

Este material se comparte con fines educativos. Si lo utilizas, por favor dale el crédito correspondiente a la autora.

---

*Última actualización: abril 2026*
