# Планирование и запуск A/B-теста

Проект представляет собой анализ двух экспериментов, проводящихся в рамках некоторого цифрового сервиса. Первый эксперимент - это <b>A/A-тест</b>. Он нужен для проверки корректности работы системы сплитования пользователей по группам. Второй эксперимент - это <b>A/B-тест</b>. В рамках него тестируется новый алгоритм рекомендаций в ленте, цель которого - увеличение <b>CTR</b> пользователей. Для анализа использовались разные статистические методы и подходы: <b>Т-тест Стьюдента</b>, <b>U-тест Манна-Уитни</b>, <b>Сглаживание CTR</b>, <b>Пуассоновский бутстреп</b>, <b>Бакетное преобразование</b>, <b>Линеаризация</b>. Проект реализован в виде двух Jupyter ноутбуков. Первый ноутбук - <b>aa_test.ipynb</b> - содержит анализ <b>AA-теста</b> и проверку системы сплитования. Второй ноутбук - <b>ab_test.ipynb</b> - анализ <b>AB-теста</b> нового алгоритма рекомендаций.


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

Для запуска анализа A/B тестов в Jupyter Notebook необходимо настроить виртуальное окружение Python и установить все зависимости проекта.

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
