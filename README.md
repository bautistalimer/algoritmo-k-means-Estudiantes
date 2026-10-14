# Segmentación de Estudiantes mediante K-Means y Estandarización de Variables

Este repositorio contiene la implementación de un modelo de aprendizaje no supervisado (**K-Means**) aplicado a un conjunto de datos multivariable de estudiantes, agrupándolos según su patrón de edad, dedicación horaria y desempeño académico.

---

## 📄 Contenido del Repositorio

* `algoritmo_k_means_2.py`: Script en Python que procesa los datos de los estudiantes, estandariza las 3 variables de entrada (`edad`, `horas_estudio`, `promedio_academico`), aplica clustering K-Means y genera una visualización 2D de los grupos resultantes.

---

## 📊 Dataset de Trabajo

El dataset está compuesto por registros individuales de **50 estudiantes**, caracterizados por tres variables numéricas:

* **`edad`**: Edad del estudiante en años.
* **`horas_estudio`**: Horas semanales dedicadas al estudio.
* **`promedio_academico`**: Promedio de calificaciones (escala de 1 a 10).

---

## ⚙️ Metodología y Algoritmo

1. **Preprocesamiento Multivariable:**
   * Escalado mediante `StandardScaler` de Scikit-Learn sobre las tres características (`edad`, `horas_estudio` y `promedio_academico`) para evitar que diferencias de escala sesguen el cálculo de distancias euclídeas.

2. **Clustering con K-Means ($k=4$):**
   * Agrupamiento no supervisado en 4 clusters ($k = 4$, `random_state = 42`).

3. **Perfilado de Clusters:**
   * **Cluster 0:** *Notas altas - mayores*
   * **Cluster 1:** *Notas bajas*
   * **Cluster 2:** *Notas altas - jóvenes*
   * **Cluster 3:** *Notas medias*

4. **Visualización 2D:**
   * Gráfico de dispersión (Scatter Plot) en Matplotlib relacionando `edad` vs. `promedio_academico`, diferenciado por colores y leyenda representativa para cada perfil identificado.

---

## 🚀 Requisitos e Instalación

### Requisitos Previos

* Python 3.x
* Librerías requeridas: `pandas`, `scikit-learn`, `matplotlib`

Instalación de dependencias:

```bash
pip install pandas scikit-learn matplotlib
