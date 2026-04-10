# Taller — Recursividad y Paradigma Divide y Vencerás

Este repositorio contiene los archivos correspondientes al taller de análisis y diseño de algoritmos,
enfocado en los conceptos de recursividad y el paradigma divide y vencerás. Se implementaron y
compararon experimentalmente cuatro algoritmos en Python, midiendo sus tiempos de ejecución para
diferentes tamaños de entrada y analizando sus comportamientos a partir de gráficas comparativas.

---

## Estructura del repositorio

```
taller-algoritmos/
│
├── README.md
│
├── notebooks/
│   ├── Ejercicio_3_subarreglo_maximo.ipynb
│   └── Ejercicio_4_merge_vs_insertion.ipynb
│
└── resultados/
    ├── grafica_subarreglo_maximo.png
    └── grafica_merge_vs_insertion.png
```

- **`notebooks/`**: contiene los dos notebooks de Jupyter con la implementación completa de los algoritmos, la medición de tiempos y las conclusiones de cada ejercicio.
- **`resultados/`**: contiene las gráficas comparativas exportadas como imágenes `.png`, generadas a partir de la ejecución de los notebooks.

---

## Descripción de los ejercicios

### Ejercicio 3 — Problema del Subarreglo Máximo (`Ejercicio_3_subarreglo_maximo.ipynb`)

Se implementaron dos algoritmos para encontrar el subarreglo contiguo de suma máxima dentro de un arreglo de enteros:

- **Fuerza bruta** — evalúa todas las combinaciones posibles de subarreglos contiguos. Complejidad: O(n²).
- **Divide y vencerás** — divide recursivamente el arreglo en mitades y considera tres casos: subarreglo máximo en la mitad izquierda, en la mitad derecha, o cruzando el punto medio. Complejidad: O(n log n).

Se midieron los tiempos de ejecución para n = 10, 50, 100, 200, 500 y 1000, con arreglos aleatorios de valores en el rango [-1000, 1000].

### Ejercicio 4 — Comparación de Algoritmos de Ordenamiento (`Ejercicio_4_merge_vs_insertion.ipynb`)

Se implementaron dos algoritmos de ordenamiento:

- **Merge Sort** — algoritmo recursivo basado en el paradigma divide y vencerás. Divide el arreglo por la mitad, ordena cada mitad recursivamente y las combina. Complejidad: O(n log n).
- **Insertion Sort** — algoritmo iterativo que construye el arreglo ordenado un elemento a la vez, insertando cada nuevo elemento en su posición correcta. Complejidad: O(n²).

Se midieron los tiempos de ejecución para n = 10, 50, 100, 500, 1000 y 5000, con arreglos aleatorios de valores en el rango [-10000, 10000].

---

## Requisitos

- Python 3.x
- Jupyter Notebook o Google Colab
- Librerías: `matplotlib`, `seaborn` (instalables con `pip install matplotlib seaborn`)

---

## Cómo ejecutar los notebooks

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/taller-algoritmos.git
   cd taller-algoritmos
   ```

2. Instalar las dependencias:
   ```bash
   pip install matplotlib seaborn
   ```

3. Abrir el notebook deseado:
   ```bash
   jupyter notebook notebooks/Ejercicio_3_subarreglo_maximo.ipynb
   ```

4. Ejecutar todas las celdas en orden con **Run All** o `Shift + Enter` celda por celda.

> También se pueden abrir directamente en **Google Colab** subiendo el archivo `.ipynb` desde la interfaz.

---

## Resultados

Las gráficas generadas por cada notebook se encuentran en la carpeta `resultados/` y muestran la comparación del tiempo de ejecución en función del tamaño de entrada para cada par de algoritmos. Estas gráficas permiten observar visualmente la diferencia en el comportamiento de algoritmos con complejidad O(n log n) frente a algoritmos con complejidad O(n²).