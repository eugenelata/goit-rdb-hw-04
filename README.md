# PostgreSQL Homework 4: Olist E-commerce

## Dataset

Використано Brazilian E-Commerce Public Dataset by Olist.

Джерело: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Дані завантажуються через KaggleHub:

```python
import kagglehub
dataset_dir = kagglehub.dataset_download("olistbr/brazilian-ecommerce")
```

## Використані таблиці

Основні таблиці:
- `olist_customers`
- `olist_orders`
- `olist_order_items`
- `olist_products`
- `olist_sellers`
- `olist_order_reviews`

Додаткові таблиці:
- `olist_customer_dim`
- `customer_segments`
- `seller_score`
- `seller_alerts`

Також використовуються відповідні `raw`-таблиці для початкового завантаження CSV.

## Запуск

1. Відкрити notebook у Google Colab.
2. Встановити залежності: `pandas`, `sqlalchemy`, `psycopg2-binary`, `kagglehub`.
3. Встановити та запустити PostgreSQL.
4. Створити базу даних `hw4_db` і налаштувати підключення.
5. Завантажити датасет Olist через KaggleHub.
6. Послідовно виконати всі комірки notebook.

## Зміст роботи

- Створення typed-таблиць із constraints.
- DML-запити: `INSERT`, `UPDATE`, `DELETE`, `RETURNING`, `ON CONFLICT`.
- Сегментація покупців.
- JOIN-запити та бізнес-аналіз.
- Агрегації, `HAVING`, set operations і window functions.

**Примітка:** замість `pgserver` використано локальний PostgreSQL у Google Colab через проблеми зі встановленням `pgserver` у Python 3.13.
