**Seaborn** — это библиотека Python, основанная на Matplotlib, которая упрощает создание сложных и информативных визуализаций данных.

#### 1. Импорт библиотеки
```python
import seaborn as sns
import matplotlib.pyplot as plt
```

#### 2. Построение графиков

- **График распределения (Distribution Plot)**:
  ```python
  data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
  sns.distplot(data)
  plt.show()
  ```

- **Гистограмма и KDE (плотность распределения)**:
  ```python
  sns.histplot(data, kde=True)
  plt.show()
  ```

- **Диаграмма разброса (Scatter Plot)**:
  ```python
  tips = sns.load_dataset("tips")
  sns.scatterplot(x="total_bill", y="tip", data=tips)
  plt.show()
  ```

#### 3. Работа с наборами данных

- **Загрузка набора данных**:
  Seaborn предоставляет несколько встроенных наборов данных:
  ```python
  tips = sns.load_dataset("tips")
  ```

- **Корреляционная матрица (Heatmap)**:
  ```python
  corr = tips.corr()
  sns.heatmap(corr, annot=True, cmap="coolwarm")
  plt.show()
  ```

#### 4. Графики категориальных данных

- **Box Plot (коробчатая диаграмма)**:
  ```python
  sns.boxplot(x="day", y="total_bill", data=tips)
  plt.show()
  ```

- **Violin Plot (скрипичная диаграмма)**:
  ```python
  sns.violinplot(x="day", y="total_bill", data=tips)
  plt.show()
  ```

- **Bar Plot (столбчатая диаграмма)**:
  ```python
  sns.barplot(x="day", y="total_bill", data=tips)
  plt.show()
  ```

#### 5. Линейные графики и регрессия

- **Линейная регрессия с доверительными интервалами**:
  ```python
  sns.lmplot(x="total_bill", y="tip", data=tips)
  plt.show()
  ```

- **График парных отношений (Pairplot)**:
  ```python
  sns.pairplot(tips)
  plt.show()
  ```

#### 6. Настройка стиля графиков

- **Изменение стиля графиков**:
  Seaborn позволяет изменять стиль отображения графиков:
  ```python
  sns.set_style("whitegrid")
  sns.scatterplot(x="total_bill", y="tip", data=tips)
  plt.show()
  ```

- **Цветовые палитры**:
  Seaborn предлагает различные палитры для цветовой настройки графиков:
  ```python
  sns.set_palette("pastel")
  sns.boxplot(x="day", y="total_bill", data=tips)
  plt.show()
  ```
