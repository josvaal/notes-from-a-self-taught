---
title: Valor Presente con Alternativas con Vidas Diferentes
tags:
  - economía
  - análisis financiero
  - valor presente
---

## Contexto
Un laboratorio de la **UNAMAD**, contratado por la **NASA**, está evaluando la economía de tres máquinas de igual servicio para sistemas espaciales de celdas de combustible a base de hidrogeno y metanol. La evaluación considera el **Valor Presente (VP)** con una **Tasa Mínima Aceptable de Rendimiento (TMAR)** de **10% anual**.

Las alternativas son:

1. Máquina a base de electricidad
2. Máquina a base de gas
3. Máquina a base de energía solar

### Datos iniciales

| Tipo                 | Costo inicial (S/.) | Costo de operación anual (S/.) | Valor de rescate (S/.) | Vida útil (años) |
|----------------------|---------------------|----------------------------------|-------------------------|--------------------|
| **Electricidad**    | 4500                | 900                              | 200                     | 8                  |
| **Gas**             | 3500                | 700                              | 350                     | 8                  |
| **Energía Solar**   | 6000                | 50                               | 100                     | 8                  |

## Fórmulas

El **Valor Presente (VP)** se calcula usando:

\[
VP = - \text{Costo Inicial} - \text{Costo de Operación Anual} \cdot (P/A, i, n) + \text{Valor de Rescate} \cdot (P/F, i, n)
\]

Donde:
- \( (P/A, i, n) \): Factor de valor presente para una anualidad
- \( (P/F, i, n) \): Factor de valor presente para un valor único
- \( i \): Tasa de interés (TMAR)
- \( n \): Período de evaluación (vida útil)

Los factores son calculados con:

1. **Valor presente para una anualidad**:
   \[
   (P/A, i, n) = \frac{1 - (1 + i)^{-n}}{i}
   \]

2. **Valor presente para un monto único**:
   \[
   (P/F, i, n) = (1 + i)^{-n}
   \]

Con \( i = 10\% \) y \( n = 8 \):
- \( (P/A, 10\%, 8) = 5.3349 \)
- \( (P/F, 10\%, 8) = 0.4665 \)

## Cálculos del Valor Presente

1. **Electricidad**:
   \[
   VP_{Electricidad} = -4500 - 900 \cdot 5.3349 + 200 \cdot 0.4665 = -9208 \, \text{S/.}
   \]

2. **Gas**:
   \[
   VP_{Gas} = -3500 - 700 \cdot 5.3349 + 350 \cdot 0.4665 = -7071 \, \text{S/.}
   \]

3. **Energía Solar**:
   \[
   VP_{Solar} = -6000 - 50 \cdot 5.3349 + 100 \cdot 0.4665 = -6220 \, \text{S/.}
   \]

### Resultados

| Alternativa         | Valor Presente (S/.) | Evaluación |
|---------------------|---------------------|-------------|
| **Electricidad**    | -9208              | No viable   |
| **Gas**             | -7071              | No viable   |
| **Energía Solar**   | -6220              | Más viable |

La alternativa más viable es la máquina a **energía solar**, ya que tiene el menor costo presente.

---

## Ejemplo con Vidas Diferentes

Una empresa planea adquirir un equipo de corte y terminado. Dos fabricantes ofrecen:

| Fabricante | Costo Inicial (S/.) | Costo de Operación Anual (S/.) | Valor de Rescate (S/.) | Vida útil (años) |
|------------|---------------------|----------------------------------|-------------------------|--------------------|
| **A**      | 15000              | 3500                            | 1000                   | 6                  |
| **B**      | 18000              | 3100                            | 2000                   | 9                  |

### Resolución

#### Período Común Múltiplo (MCM)

La vida útil de las máquinas es diferente, por lo que se utiliza el MCM:
\[
MCM = \text{mínimo común múltiplo de } 6 \text{ y } 9 = 18 \, \text{años}
\]

Se calcula el VP repitiendo cada máquina hasta completar el MCM:

1. **Fabricante A (MCM = 18)**:
   \[
   VP_{A} = -15000 - 3500 \cdot (P/A, 15\%, 18) + 1000 \cdot (P/F, 15\%, 18)
   \]
   \[
   VP_{A} = -45036 \, \text{S/.}
   \]

2. **Fabricante B (MCM = 18)**:
   \[
   VP_{B} = -18000 - 3100 \cdot (P/A, 15\%, 18) + 2000 \cdot (P/F, 15\%, 18)
   \]
   \[
   VP_{B} = -41384 \, \text{S/.}
   \]

### Resultados

| Fabricante | Valor Presente (S/.) | Evaluación |
|------------|---------------------|-------------|
| **A**      | -45036             | No viable   |
| **B**      | -41384             | Más viable |

El fabricante **B** es la mejor opción debido al menor valor presente.
