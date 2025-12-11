# Планирование и запуск A/B-теста

Проект — это анализ двух экспериментов в нашем сервисе, который помог проверить, насколько надёжно работает система распределения пользователей, и оценить эффективность нового алгоритма рекомендаций.

В первой части, в рамках <b>A/A-теста</b>, мы проверили корректность системы сплитования — действительно ли пользователи распределяются в группы <b>случайно</b> и <b>равномерно</b>. Это важный этап перед запуском настоящих изменений.

Во второй части, в <b>A/B-тесте</b>, мы протестировали новый алгоритм рекомендаций для ленты, цель которого — повысить кликабельность (<b>CTR</b>). Для анализа используется набор методик: как классические статистические тесты Стюдента и Манна-Уитни, так и Сглаживание, Poisson Bootrstrap, Bucket Transformation и Linearization. 

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/pandas-2.2.2+-orange" alt="pandas">
  <img src="https://img.shields.io/badge/numpy-1.26.4+-blue" alt="numpy">
  <img src="https://img.shields.io/badge/scipy-1.13.1+-orange" alt="scipy">
  <img src="https://img.shields.io/badge/pingouin-0.5.5+-blue" alt="pingouin">
  <img src="https://img.shields.io/badge/matplotlib-3.9.2+-orange" alt="matplotlib">
  <img src="https://img.shields.io/badge/seaborn-0.13.2+-blue" alt="seaborn">
</p>

## Навигация 
1. [Описание проекта](#навигация)
2. [Установка](#установка)

## Установка

Для запуска в Jupyter Notebook необходимо настроить виртуальное окружение Python и установить все зависимости проекта.

### 1. Клонирование репозитория
```bash
# Клонируем репозиторий
git clone https://github.com/idBulenkoIvan/ab_test.git

# Переходим в директорию проекта
cd ab_test

# Проверяем наличие файлов
ls -la
```

### 2. Создание и активация виртуального окружения
```bash
# Создаем виртуальное окружение
python -m venv venv

# Активируем
venv\Scripts\activate
```

### 3. Установка зависимостей
```bash
# Устанавливаем необходимые пакеты
pip install -r requirements.txt
```

### 4. Настройка Jupyter ядра
```bash
# Установливаем ядро для Jupyter
python -m ipykernel install --user --name=venv --display-name="Python (venv)"
```
