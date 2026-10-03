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
### 0. Установка pip, venv и git
##### Проверка git

```bash
git --version
```

Если команда не найдена:

- **Windows**: скачайте установщик с [git-scm.com](https://git-scm.com/download/win) и запустите его.После установки перезапустите терминал.
- **Linux (Ubuntu / Debian)**:

```bash
sudo apt update
sudo apt install git
```

- **macOS**: `brew install git`.

После установки снова выполните `git --version`

##### Проверка python
```bash
python --version      # Windows
python3 --version     # Linux / macOS
```
Нужна версия 3.12 или выше. Если команда не найдена, скачайте Python с [python.org](https://www.python.org/downloads/). На Windows при установке отметьте галочку **Add python.exe to PATH**.

##### Проверка pip
```bash
python -m pip --version      # Windows
python3 -m pip --version     # Linux / macOS
```

###### Если `pip --version` не дал ответа

Установите `pip`:

```bash
# Windows / macOS
python -m ensurepip --upgrade
python -m pip install --upgrade pip

# Ubuntu / Debian
sudo apt update
sudo apt install python3-pip python3-venv
```

После установки снова проверьте:

```bash
pip --version
```

##### Проверка venv
```bash
python -m venv --help      # Windows
python3 -m venv --help     # Linux / macOS
```

##### Создайте виртуальное окружение:

```bash
# Windows (PowerShell)
python -m venv .venv
.venv\Scripts\Activate.ps1

# Linux / macOS / WSL
python3 -m venv .venv
source .venv/bin/activate

# FISH -> Linux / macOS / WSL
python3 -m venv .venv
source .venv/bin/activate.fish
```
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
git clone https://github.com/YukiTheKilla/spbu_ml_2026 .
poetry install
```

### 3. Запуск

```bash
# активировать окружение
poetry env activate

# запустить Jupyter
poetry run jupyter lab
```

После открываем через jupyter файл `/notebooks/main.ipynb`