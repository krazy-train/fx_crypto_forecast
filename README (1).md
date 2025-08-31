# Прогнозирование цены Ethereum (ETH) на один день вперед

Этот проект решает задачу прогнозирования дневной лог-доходности и цены Ethereum на следующий день (t+1) с использованием машинного обучения.

## Описание проекта

Проект включает в себя:
*   Загрузку и первичный анализ исторических данных по Ethereum.
*   Создание набора признаков (feature engineering), включая лаги, технические индикаторы и календарные features.
*   Обучение и оценку моделей машинного обучения (Ridge и HistGradientBoostingRegressor).
*   Анализ важности признаков и оценку качества прогноза как на доходностях, так и на конечной цене.

## Технологический стек

*   **Язык программирования:** Python
*   **Основные библиотеки:** pandas, numpy, scikit-learn, matplotlib, seaborn, joblib
*   **Среда разработки:** Jupyter Notebook

## Установка и запуск

1.  **Клонируйте репозиторий:** 
    ```bash
    git clone <https://github.com/krazy-train/fx_crypto_forecast.git>
    cd ethereum-forecast
    ```

2.  **Установите зависимости:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Загрузите данные:**
    *   Скачайте датасет `coin_Ethereum.csv` с [Kaggle](https://www.kaggle.com/datasets/sudalairajkumar/cryptocurrencypricehistory).
    *   Поместите файл в директорию `data/`.

4.  **Запустите Jupyter Notebook и откройте ноутбук:**
    ```bash
    jupyter notebook
    ```
    *   Перейдите в папку `notebooks/` и откройте `01_fx_crypto_forecast.ipynb`.
    *   Выполните все ячейки (Cell -> Run All).

## Метрики и результаты

Модели оцениваются по следующим метрикам:
*   **Для прогноза доходности:** RMSE, MAE, R²
*   **Для прогноза цены (после преобразования):** RMSE, MAE, MAPE
*   **Точность направления:** Процент правильных предсказаний направления движения цены (вверх/вниз)

## Модель

Основная модель для прогнозирования — `HistGradientBoostingRegressor` из библиотеки scikit-learn. Обученная модель сохраняется в файл `models/ethereum_return_model_hgbr.joblib` для последующего использования.



