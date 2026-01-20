# Анализ пользовательской активности в Instagram

## Описание проекта
Проект представляет собой учебный Data Engineering пайплайн для анализа
синтетических данных, имитирующих поведение пользователей Instagram.

Реализован полный цикл работы с данными:
- Extract
- Transform
- Load
- Exploratory Data Analysis (EDA)
- Визуализация результатов через Streamlit

## Датасет
Используется синтетический датасет с Kaggle:

**Social Media User Behavior & Lifestyle – Instagram**
  
Ссылка на датасет:  
https://drive.google.com/file/d/1HvdWy3m5SS66i3AV5V0k1Osu3RkKTbaV/view?usp=sharing

Файл для работы:
instagram_usage_lifestyle.csv


## Структура проекта
```
data/
raw/ # исходные данные (не хранятся в git)
processed/ # обработанные данные (не хранятся в git)
experiments/
eda.ipynb # исследовательский анализ данных
src/
etl/
extract.py
transform.py
load.py
pipeline.py
cli.py
streamlit_app/
app.py
requirements.txt
README.md
```
## Установка зависимостей
```bash
pip install -r requirements.txt
```

Запуск ETL-пайплайна
python -m src.cli \
  --input data/raw/instagram_usage_lifestyle.csv \
  --output data/processed

Запуск EDA
jupyter notebook experiments/eda.ipynb

Запуск Streamlit-приложения
streamlit run streamlit_app/app.py

Используемые технологии

Python 3.11

pandas

seaborn / matplotlib

Streamlit

Parquet
