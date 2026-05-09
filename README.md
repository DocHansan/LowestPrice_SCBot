![Main screen](readme_img/statistics_2024-2025.jpg)

За 8 месяцев было отфармлено 2.9ккк игровых рублей на 2-х машинах, торговались продвинутые запчасти (приоритет) и ивентовые кейсы  
Стратегия - поштучная покупка ниже рынка, продажа стаков 50, 100 штук с наценкой  
Минусы - именные предметы, которые приходилось продавать через Discord / чат игры  
---
Торговый бот для игры Stalcraft (Steam-версия)

Скрипт предназначен для автоматической работы с аукционом в Steam-версии Stalcraft. Он открывает аукцион, следит за его работой и периодически перезапускает игру для стабильности.  
Как использовать:
* Запустите игру через Steam и зайдите на нужный сервер.
* Запустите main.py.
* Переключитесь в окно игры (бот взаимодействует напрямую).

Бот сам откроет аукцион и будет торговать в фоновом режиме.  

Поддерживается автоматический перезапуск клиента Steam при сбоях или вылетах.  
Требуется стабильное соединение и подходящее разрешение экрана.  

Настройка бота  
Все настройки выполняются в блоке # BOT CONTROL START, это самый важный блок скрипта:
* paths: массив путей к разным версиям Steam (steam.exe).
* steam_path: индекс используемой Steam-версии в массиве paths.
* items: список торгуемых предметов.
* items_prices: массив цен, соответствующих предметам из items.
* item_index: индекс выбранного предмета в items, которым бот будет торговать при запуске.
* auction_button: клавиша открытия аукциона — не забудьте настроить под себя!
---

Trading bot for Stalcraft (Steam version)

This script is designed to automate trading through the auction in the Steam version of Stalcraft. It opens the auction, manages trading, and periodically restarts the game client for stability.  
How to use:
* Launch the game via Steam and enter the desired server.
* Run main.py.
* Tab into the game window — the bot interacts with it directly.

The bot will automatically open the auction and trade in the background.  

Automatic restarts of the Steam client are supported in case of crashes.  
Requires a stable internet connection and proper screen resolution.  

Bot Configuration  
All configuration is done in the # BOT CONTROL START section — this is the most important part of the script:
* paths: array of paths to different steam.exe installations.
* steam_path: index of the Steam version to use from paths.
* items: array of tradeable item names.
* items_prices: array of prices corresponding to items.
* item_index: index of the item to trade on script launch.
* auction_button: key used to open the auction — make sure to set it properly!
---

Версия Python 3.12

Виртуальная среда:
* Установка
    * pip install virtualenv
* Создание виртуальной среды
    * python -m venv venv
* Активация виртульной среды
    * cmd: .\Scripts\activate
    * VS Code: Ctrl+Shift+P, команда "Python: Select Interpreter"

Установка библиотек: pip install -r requirements.txt  
Установка tesserocr:
* Официальный репозиторий: https://github.com/sirfz/tesserocr  
Если версия Python отличается, следовать инструкции по установке в репозитории
* Установить tesserocr.whl файл (\Tesserocr) (для версии 3.12)
* Добавить в переменные среды TESSDATA_PREFIX, указать путь "\Tesserocr\Models"  
Консольная команда  
setx TESSDATA_PREFIX %\...\Tesserocr\Models%

Требования для работы бота:
* Разрешение экрана 1920*1080
* Панель задач Windows всегда активна
* Игра должна быть в окне с рамкой на весь экран
