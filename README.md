# 🛒 From Click to Delivery: Brazilian E-Commerce Unboxed

**Kaggle Notebook:** [Let’s Talk E-Commerce: The Brazilian Edition](https://www.kaggle.com/code/sergeistanislavovich/let-s-talk-e-commerce-the-brazilian-edition)
**Dataset:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## 🚀 Project Kickoff — “From Click to Delivery: What Really Happens?”

This project dives into the entire customer journey in Brazilian e-commerce — from first click to final review. Not just sales figures, but **what really works**, **what breaks**, and **where the friction hides**.

We replaced assumptions with numbers. And guesswork — with insights.

---

## 🧭 Project Roadmap

1. **EDA Phase**
   – Understand customer behavior, reviews, delays, and product categories
2. **Metric Analysis**
   – Core KPIs: conversion, retention, LTV, delivery timing
3. **Hypothesis Testing**
   – What’s real vs. noise? We used non-parametric tests to find out
4. **Growth Ideas**
   – Actionable insights based on real patterns

---

## 📦 Dataset Integration

After merging 8+ tables into a clean dataset of **119,141 records**, we conducted full integrity checks:

* Missing values explained (mostly legit: cancellations, no review)
* Data types normalized (e.g., timestamps, categories)
* Geo-coordinates imputed via medians
* No duplicate or mismatched joins found

**Result:** rock-solid foundation for analysis.

---

## 🔍 Highlights from EDA

### 📐 Order Size Matters

* 1–2 items = 90% of orders, but unstable in delivery & review
* Larger orders → more predictable delivery, worse ratings
* Suggestion: treat large baskets as high-risk/high-value

### 🌟 Reviews (avg: 4.08 / 5)

* 54% of **1-star reviews** caused by **late delivery**
* 8.5% happen **even when early** — so timing isn’t everything
* 8.2% reviews left **before delivery** 🤔
* Ratings drop with complexity (multi-item orders)

### 📊 Business Metrics

| Metric         | Value            | Insight                                     |
| -------------- | ---------------- | ------------------------------------------- |
| Conversion     | 98.9%            | Great! But mostly logistics, not marketing  |
| Retention      | 3%               | 🚨 Danger zone — needs CRM/loyalty fixes    |
| AOV            | 171.8 R\$        | Very wide spread — IQR average is 113.3 R\$ |
| ARPU           | 213.0 R\$        | Skewed by few big spenders — classic 80/20  |
| LTV            | Median 113.1     | Top 5 customers = 30K–109K R\$ each 🤯      |
| Early delivery | Avg: 12 days     | Looks nice, but might mislead customers     |
| Shipping delay | Median: 7.1 days | Main bottleneck — only 26.4% < 7d           |

---

## 🧪 Hypothesis Testing (Non-parametric)

| Hypothesis                          | Test                  | Result                                       |
| ----------------------------------- | --------------------- | -------------------------------------------- |
| Late delivery → worse reviews       | Mann–Whitney U        | ✅ Confirmed (p < 0.0001)                     |
| Payment method affects value        | Kruskal–Wallis + Dunn | ✅ Confirmed (p < 0.001)                      |
| More items → worse reviews          | Mann–Whitney U        | ✅ Confirmed                                  |
| Popular categories → better reviews | Mann–Whitney U        | 🟡 Not statistically significant (p = 0.086) |

---

## 💡 Strategic Takeaways

* **Delivery = product experience**. It defines perception.
* **Retention is a crisis.** Fix it or forget growth.
* **High-value customers are few** — find them, keep them.
* **Bigger orders need more love.** They're riskier.
* **Voucher use = underutilized**. Run those promos.

---

## ✅ Next Steps

* Segment reviews by category and item count
* Model satisfaction using delivery + complexity
* Improve ETA accuracy (less under-promise, more trust)
* Run A/B tests on payment flow and shipping options

---

## 📍 Final Words

Brazil’s e-commerce looks sleek, but behind the scenes, **logistics, retention, and trust** drive the real results. This project builds the analytical lens to **see what’s really going on** — and where to push next.

---



---

# 🛒 От клика до доставки: что на самом деле происходит?

## 🔍 Исследуем e-commerce в Бразилии

Этот проект — не просто анализ продаж. Мы глубоко копаем путь клиента: от просмотра товара до финального отзыва. Где теряются заказы? Почему уходят клиенты? Что реально влияет на оценки?

Цель — не гадать, а понять:

> Как продавать больше, доставлять лучше и удерживать клиентов?

---

## 📊 Структура проекта

1. **Загрузка данных и первичная проверка**
   Проверка пропусков, объединение таблиц, очистка, нормализация.
   ➕ Получена финальная таблица: **119,141 записей, 22 столбца**

2. **EDA: Понимание поведения клиентов**

   * Оценки: от чего зависят 1-звёздочные отзывы
   * Категории: кто приносит деньги
   * Оплаты: карты, наличка, ваучеры
   * Задержки и их цена

3. **Метрики: Что говорят числа**

   * 📦 Средний чек (AOV): **172 BRL**
   * 🔄 Повторные заказы: **3%** — тревожный звоночек
   * ⏱ Доставка: в среднем на **12 дней раньше**
   * 🌟 Оценка: **4.08 / 5**, но 54% 1-звёзд — из-за доставки

4. **Гипотезы и A/B-анализы**
   ✅ Задержка → хуже отзывы
   ✅ Метод оплаты влияет на сумму
   ✅ Большие заказы — больше проблем
   ⛔️ Популярность категории ≠ лучшие оценки

5. **Итоги и идеи роста**

   * Улучшить прогноз ETA (доверие растёт)
   * Ретаргетинг по категориям с низкой оценкой
   * Внедрить рекомендации и A/B тесты в оплате и доставке
   * Персонализировать работу с крупными заказами

---

## 📎 Полезные ссылки

* 📂 [Проект на Kaggle](https://www.kaggle.com/code/sergeistanislavovich/let-s-talk-e-commerce-the-brazilian-edition)
* 📦 [Датасет: Brazilian E-Commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

## 🧠 Финальные выводы

> Бразильский e-commerce выглядит гладко — но внутри скрыто множество точек роста.

* Доставка — главный источник негатива
* Оплата влияет не только на удобство, но и на итоговую сумму
* Усложнение заказа = риск недовольства
* Нужна умная сегментация: 1 товар, 2–4, 5+ — поведение меняется

---

💡 **Данные ≠ догадки.**
Мы хотим заменить интуицию — доказательствами.
