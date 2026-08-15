# Документация: оплата и доставка

Документация описывает **текущую реализацию** в коде (Laravel 10), а не внешние гайды провайдеров.

## Содержание

| Файл | Тема |
|------|------|
| [01-payments.md](01-payments.md) | Архитектура платежей: интерфейс, фабрика, роуты, checkout |
| [02-payments-paysera.md](02-payments-paysera.md) | PaySera: WebToPay, callback, список банков/карт |
| [03-shipping.md](03-shipping.md) | Архитектура доставки: интерфейс, тарифы, pickup points, админка |
| [04-shipping-omniva.md](04-shipping-omniva.md) | Omniva: PU/QH, SDK `mijora/omniva-api`, синхронизация локеров |
| [05-http-header.md](05-http-header.md) | HTTP-заголовки приложения и Omniva `ShipmentHeader` |

## Ключевые пакеты

- Платежи PaySera: `webtopay/libwebtopay` (`WebToPay`)
- Доставка Omniva: `mijora/omniva-api` (`Mijora\Omniva\...`)

## Логи

- Платежи: канал `payment` → `storage/logs/laravel-payment.log`
- Доставка: канал `shipping` → `storage/logs/laravel-shipping.log`
