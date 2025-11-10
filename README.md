# Steiner Tree - Algoritmo de Dreyfus-Wagner

Trabajo práctico integrador de **Teoría de la Computación II (TEOII)** - Universidad Nacional de Luján, 2025.

## 📋 Descripción

Este proyecto implementa el **algoritmo de Dreyfus-Wagner** para resolver el problema del **Steiner Tree** en grafos ponderados:

### 🌳 Problema del Steiner Tree

Dado un grafo ponderado G = (V, E) y un conjunto de nodos terminales K ⊆ V, encontrar el árbol de peso mínimo que conecte todos los terminales K (pudiendo usar nodos intermedios de Steiner).

## 🎯 Algoritmo Implementado

### **Dreyfus-Wagner (1971)**

- Algoritmo exacto basado en programación dinámica
- **Complejidad:** O(3^|K| × n²) donde |K| = número de terminales
- Parametrizado por el número de terminales
- **Práctico para:** |K| ≤ 12-15 terminales
- Exploración exhaustiva de subconjuntos de terminales mediante técnica de divide y conquista

## 📊 Características

- ✅ Implementación completa del algoritmo Dreyfus-Wagner
- ✅ Visualización gráfica de soluciones
- ✅ Casos de prueba variados (grafos aleatorios, completos, sparse)
- ✅ Análisis de complejidad temporal empírica
- ✅ Comparación con MST (Minimum Spanning Tree) como baseline

## 🚀 Instalación

### Requisitos Previos

- Python 3.8 o superior
- pip

### Instalación de Dependencias

```bash
pip install -r requirements.txt
```

Las dependencias principales son:

- `numpy` - Operaciones numéricas
- `matplotlib` - Visualización de grafos
- `networkx` - Manipulación de grafos
- `scipy` - Algoritmos de optimización
- `jupyter` - Entorno de notebooks

## 💻 Uso

### Ejecutar el Notebook

```bash
jupyter notebook src/dreyfus_wagner-multiway.ipynb
```

O abrir directamente en VS Code con la extensión de Jupyter.

### Estructura del Notebook

1. **Importaciones y configuración**
2. **Implementación del algoritmo Dreyfus-Wagner**
3. **Funciones auxiliares** (visualización, generación de grafos)
4. **Casos de prueba**
   - Grafos pequeños (8, 10, 12 nodos)
   - Grafos completos
   - Grafos sparse (dispersos)
   - Grafos grandes
5. **Análisis de resultados**
   - Tiempos de ejecución
   - Escalabilidad
   - Comparación con MST
6. **Conclusiones**

## 📈 Resultados

El notebook incluye análisis detallados que demuestran:

- **Dreyfus-Wagner** encuentra la solución óptima exacta
- El rendimiento depende exponencialmente del número de terminales
- MST ofrece una cota superior rápida pero generalmente subóptima
- Visualización clara de las diferencias entre el árbol de Steiner óptimo y el MST
