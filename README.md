# 🌐 Language / Язык

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## <a name="russian"></a>

# Shiny_Churn_Prediction

## 📌 О проекте

Проект выполнен в рамках курса **"Приложения и практика анализа данных"** (Майнор НИУ ВШЭ, 4 семестр).

**Задача:** переработать проект по анализу оттока клиентов банка в интерактивное Shiny-приложение.

**Что сделано:**
- Обучена модель логистической регрессии (предсказание оттока по возрасту, балансу и количеству продуктов)
- Создано Shiny-приложение с пользовательским вводом
- Приложение опубликовано на **shinyapps.io**

## 📁 Содержимое репозитория

| Файл | Описание |
|------|----------|
| `analysis.Rmd` | Исходный код отчёта |
| `report.html` | HTML-отчёт с описанием приложения |
| `Задание.png` | Скриншот задания |

## 🔍 Функциональность приложения

Пользователь может ввести параметры клиента:

| Параметр | Диапазон | Описание |
|----------|----------|----------|
| **Возраст** | 18–100 лет | Возраст клиента |
| **Баланс на счёте** | от 0 | Текущий баланс |
| **Количество продуктов** | 1–10 | Число продуктов банка у клиента |

**Результат предсказания:**
- Вероятность оттока (0–1)
- Категориальный прогноз: *"Скорее останется"* или *"Скорее уйдёт"*

## 🧠 Логика модели

> *"Если у клиента много денег на счету, но он приобрёл только один продукт банка, значит он в нём не заинтересован и уйдёт. Тем более, что он молодой и готов познавать мир."*

Модель логистической регрессии учитывает:
- **Возраст** — молодые клиенты более склонны к оттоку
- **Баланс** — высокий баланс без использования продуктов = риск
- **Количество продуктов** — чем меньше продуктов, тем выше риск

## 🚀 Ссылка на приложение

🔗 **https://dpodolin.shinyapps.io/dfddd/**

## 📊 Модель

- **Тип:** логистическая регрессия
- **Признаки:** Age, Balance, NumOfProducts
- **Целевая переменная:** Exited (1 — ушёл, 0 — остался)

## 🛠 Инструменты

- R
- SQL
- Shiny
- tidymodels
- shinyapps.io (деплой)

## 📌 Автор

Подолин Дмитрий  
НИУ ВШЭ, курс "Приложения и практика анализа данных"

---

## <a name="english"></a>

# Shiny_Churn_Prediction

## 📌 About the project

The project was completed as part of the **"Applications and Practice of Data Analysis"** course (HSE Minor, 4th semester).

**Task:** redesign the bank customer churn analysis project into an interactive Shiny application.

**What was done:**
- Trained a logistic regression model (predicting churn based on age, balance, and number of products)
- Created a Shiny application with user input
- Application published on **shinyapps.io**

## 📁 Repository contents

| File | Description |
|------|-------------|
| `analysis.Rmd` | Report source code |
| `report.html` | HTML report describing the application |
| `Задание.png` | Screenshot of the assignment |

## 🔍 Application functionality

The user can enter client parameters:

| Parameter | Range | Description |
|-----------|-------|-------------|
| **Age** | 18–100 years | Client's age |
| **Balance** | ≥ 0 | Current balance |
| **Number of products** | 1–10 | Number of bank products the client has |

**Prediction result:**
- Churn probability (0–1)
- Categorical prediction: *"Likely to stay"* or *"Likely to churn"*

## 🧠 Model logic

> *"If a client has a lot of money in their account but has purchased only one bank product, it means they are not interested in it and will leave. Especially if they are young and ready to explore the world."*

The logistic regression model considers:
- **Age** — younger clients are more prone to churn
- **Balance** — high balance without using products = risk
- **Number of products** — the fewer products, the higher the risk

## 🚀 Application link

🔗 **https://dpodolin.shinyapps.io/dfddd/**

## 📊 Model

- **Type:** logistic regression
- **Features:** Age, Balance, NumOfProducts
- **Target variable:** Exited (1 — churned, 0 — stayed)

## 🛠 Tools

- R
- SQL
- Shiny
- tidymodels
- shinyapps.io (deployment)

## 📌 Author

Dmitrii Podolin  
HSE University, "Applications and Practice of Data Analysis" course
