Материалы курса по машинному обучению (СПбГУ, 2026).

## Датасет

[House Price (Kaggle)](https://www.kaggle.com/datasets/juhibhojani/house-price/data)

Скачать данные через Kaggle CLI:

```bash
kaggle datasets download -d juhibhojani/house-price -p data --unzip
```

Или вручную скачать архив по ссылке выше и положить файлы в папку `data/`: `data/house_prices.csv`.

## Тема доклада:

- **SVD (Singular Value Decomposition)**: сингулярное разложение матрицы `A = USVᵀ`, геометрический смысл, низкоранговое приближение.
- **PCA (Principal Component Analysis)**: метод главных компонент, связь с ковариационной матрицей и SVD, доля объяснённой дисперсии, выбор числа компонент.
- Применение PCA к данным о ценах на жильё: стандартизация признаков, визуализация, влияние на качество модели.

## Установка

### 1. Установка Poetry

```bash
pip install poetry
```

Проверка установки:

```bash
poetry --version
```

### 2. Установка зависимостей проекта

```bash
git clone <https://github.com/YukiTheKilla/spbu_ml_2026>
cd spbu_ml_2026
poetry install
```

### 3. Запуск

```bash
# активировать окружение
poetry env activate

# запустить Jupyter
poetry run jupyter lab
```