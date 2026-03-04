[🇬🇧 English](README.md) | [🇷🇺 Русский](README_RU.md)

# WakeLink

<div align="center">

<img src="https://raw.githubusercontent.com/wakelinkdev/.github/main/assets/wakelink-logo-white.svg" alt="WakeLink Logo" width="200">

### Безопасное удалённое управление компьютерами

[![Protocol](https://img.shields.io/badge/protocol-EWSP%20v1.0-6366f1?style=for-the-badge)](https://github.com/wakelinkdev/ewsp)
[![Encryption](https://img.shields.io/badge/encryption-XChaCha20-10b981?style=for-the-badge)](https://github.com/wakelinkdev/ewsp)
[![License](https://img.shields.io/badge/license-NGC%20v1.0-f59e0b?style=for-the-badge)](LICENSE)

[Документация](https://wakelink-project.org/docs) • [Быстрый старт](#-быстрый-старт) • [Участие в разработке](https://github.com/wakelinkdev/.github/blob/main/CONTRIBUTING.md)

</div>

---

## О проекте

**WakeLink** — безопасная система удалённого управления компьютерами со сквозным шифрованием. Пробуждайте устройства из любой точки мира с использованием криптографии военного уровня.

### Возможности

- 🖥️ **Wake-on-LAN** — пробуждение устройств по сети
- 🔐 **Сквозное шифрование** — XChaCha20 + HMAC-SHA256
- 🌐 **Двойной режим** — локальный TCP или облачный WebSocket (TLS)
- ⛓️ **Защита от повторов** — блокчейн-цепочка пакетов
- 🔑 **Прямая секретность** — сессионные ключи с ротацией

---

## Репозитории

<table>
<tr>
<td width="50%">

### 🔧 Ядро

| Репозиторий | Описание |
|:-----------|:------------|
| [**ewsp**][ewsp-core] | Криптографическая библиотека на C (протокол EWSP) |
| [**firmware**][firmware] | Прошивка ESP8266/ESP32 |

</td>
<td width="50%">

### 📱 Клиенты

| Репозиторий | Платформы |
|:-----------|:----------|
| [**cli**][client] | Windows, macOS, Linux |
| [**android**][android] | Android 7.0+ |
| [**multiplatform**][kmp] | iOS, Android, Desktop |

</td>
</tr>
</table>

### 📚 Ресурсы

| Репозиторий | Описание |
|:-----------|:------------|
| [**docs**][docs] | Документация → [wakelink-project.org/docs](https://wakelink-project.org/docs) |

[ewsp-core]: https://github.com/wakelinkdev/ewsp
[firmware]: https://github.com/wakelinkdev/firmware
[client]: https://github.com/wakelinkdev/cli
[android]: https://github.com/wakelinkdev/android
[kmp]: https://github.com/wakelinkdev/multiplatform
[docs]: https://github.com/wakelinkdev/docs

---

## 🚀 Быстрый старт

```bash
# Установка CLI
pip install cli

# Поиск устройств
wakelink scan

# Сопряжение устройства
wakelink pair 192.168.1.100

# Пробуждение ПК
wakelink wake
```

---

## 🏗️ Архитектура

```
┌──────────────────────────────────────────────────────────────────┐
│                           КЛИЕНТЫ                                 │
│   ┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────────────┐  │
│   │   CLI   │   │ Android │   │   iOS   │   │     Desktop     │  │
│   └────┬────┘   └────┬────┘   └────┬────┘   └────────┬────────┘  │
│        └─────────────┴─────┬───────┴─────────────────┘           │
│                            ▼                                      │
│                ┌───────────────────────┐                         │
│                │      ewsp-core        │                         │
│                │  XChaCha20 + HMAC     │                         │
│                └───────────┬───────────┘                         │
└────────────────────────────┼─────────────────────────────────────┘
                             │
              ┌──────────────┴──────────────┐
              ▼                             ▼
       ┌─────────────┐             ┌────────────────┐
       │   TCP:99    │             │  WSS (Cloud)   │
       │   Локальный │             │  wakelink.io   │
       └──────┬──────┘             └───────┬────────┘
              │                            │
              └────────────┬───────────────┘
                           ▼
                  ┌─────────────────┐
                  │    ESP8266/32   │
                  │    Прошивка     │
                  └─────────────────┘
```

---

## 🔒 Безопасность

| Функция | Описание |
|:--------|:------------|
| **XChaCha20** | Потоковый шифр с 24-байтовым nonce |
| **HMAC-SHA256** | Аутентификация пакетов |
| **HKDF** | Деривация ключей с разделением |
| **Blockchain Chain** | Защита от атак повторного воспроизведения |
| **Прямая секретность** | Сессионные ключи с ротацией |
| **Constant-Time** | Защита от атак по времени |

---

## 🤝 Участие в разработке

Мы приветствуем вклад сообщества! Смотрите наше [Руководство по участию](https://github.com/wakelinkdev/.github/blob/main/CONTRIBUTING.md) для получения подробностей.

**Обнаружили уязвимость?** Пожалуйста, напишите на security@wakelink.io вместо того, чтобы открывать публичный issue.

---

## 📄 Лицензия

WakeLink распространяется по лицензии **NGC v1.0**.  
По вопросам коммерческого лицензирования обращайтесь: license@wakelink.io

---

<div align="center">

**[Сайт](https://wakelink-project.org)** • **[Документация](https://wakelink-project.org/docs)** • **[Discord](https://discord.gg/wakelink)**

Сделано с ❤️ автором [@deadboizxc](https://github.com/deadboizxc)

</div>
