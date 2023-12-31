---
Publishing date: "2023-08-04 15:34"
Category: "Статья"
title: "CLV (Customer Lifetime Value)"
tags:
- "business metrics"
- "бизнес метрики"
- "метрики"
- metrics
- clv
- ltv
aliases:
- "жизненная ценность клиента"
---
## Определение
**В общем случае CLV** - это количество денег, которое клиент принесет за всю жизнь в компании (можно считать *выручку с клиента*, а можно *считать прибыль*, т.е. с  *учетом затрат* на каждого клиента).
> CLV - [[Wiki/business_metrics/PV|приведенная стоимость]] всех будущих денежных потоков, относящихся к клиенту в течение всего периода его отношений с компанией

Обычно CLV - это прогнозная величина, но можно посчитать исторический CLV следующим образом: взять клиента в момент времени $t$ и посчитать, сколько он принес денег за период времени $[0..t]$. Таким образом получим фактический CLV на момент времени $t$.
## Как прогнозировать CLV
### Пример простого прогнозирования CLV

Если предположить, что мы знаем средний размер транзакции клиента, знаем средний период жизни и среднее количество транзакций за период, то можно посчитать CLV клиента, как \[3]:
$$CLV=Average Transaction Value * Number Of Transaction * Retention Period$$
### Подход к прогнозированию CLV на горизонт с учетом дисконтирования и удержания
- $GC$ - количество денег, которое клиент приносит за один год (gross contribution per customer)
- $M$ - количество денег, которое затрачивается на удержание одного клиента в год
- $T$ - горизонт предсказания в годах
- $r$ - годовой [[Wiki/business_metrics/Retention rate|коэффициент удержания клиентов]]
- $d$ - годовой [[Wiki/business_metrics/Discount rate|коэффициент дисконтирования]]
$$CLV = GC*\sum_{t=1}^{T}{\frac{r_t}{(1+d)^t}} - M*\sum_{t=1}^{T}{\frac{r_{t-1}}{(1+d)^{t-0.5}}}$$
### Простая модель прогнозирования CLV
Часто необходимо оценить CLV клиента более быстро, чтобы сделать начальные оценки сегментов клиентов для таргетинга. Если годовая выручка с клиента относительно фиксированная, то CLV можно оценить с помощью простой модели, предполагая, что $n \to \infty$:
$$CLV = GC * \frac{r}{1 + d - r}$$


## Как используются знания о CLV
- принятие решений о привлечении клиента с учетом затрат на привлечение (если стоимоть привлечения больше, чем потенциальный CLV клиента, то нет смысла его привлекать в продукт)
- используется в расчете [[Wiki/business_metrics/Customer Equity|клиентского капитала]]
- мониторинг влияния менеджерских стратегий и иаркетинговых компаний на CLV клиентов
- определение оптимального уровня затрат на инвестиции в маркетинг и продажи
- поощрение маркетологов за привлечение долгосрочных клиентов вместо привлечения "дешевых" клиентов, которые быстро уйдут
- хорошая база для сегментации клиентов и для принятия решений по выбору стратегии в отношении клиентов
- мера для определения лояльности клиентов

## Примеры
## Связи
- [[Wiki/business_metrics/NPV|NPV]]
- [[Wiki/business_metrics/PV|PV]]

## Ссылки
- \[1] [clv wikipedia](https://en.wikipedia.org/wiki/Customer_lifetime_value)
- \[2] [clv_perdiction](https://github.com/am-aditya/Artificial-Intelligence-for-Banking/blob/master/03_ipy_notebooks/clv_prediction.ipynb)
- \[3] [customer lifetime value](https://www.netsuite.com/portal/resource/articles/ecommerce/customer-lifetime-value-clv.shtml)
