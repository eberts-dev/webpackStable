# Webpack 5 бандл

* Использует `webpack-merge`, позволяет создавать любые сборки через систему конфигов. 
* Все `plugins` и `loaders` вынесены и описаны для переиспользования

## Поддерживает

* SCSS/SASS
* SVG Sprite,
* Pug templates
* HTML loader
* Javascript (babel)
* Fonts loader
* Images loader
* Video loader
* есть SWIPER

## Старт

```shell
    npm i
    npm run build
    npm run build:dev
    npm run dev
```

## Структура
```
├── src                 
  └── assets/                   # SASS/SCSS/CSS и JS файлов
      └── js/     
          ├── spec/ 
              ├── index.js/     # подключения специфичных функции
              ├── icons.js/     # подключения SVG иконок для преобразования в sprite лист
          ├── fixes/ 
              ├── index.js/     # файл для подключения фиксов
              ├── vh-fix.js     # фикс высоты для мобильных устройств
          └── index.js/         # корневой файл
      ├── scss/
      ├── components/           # компоненты
      ├── layout/               # cтили каркаса страницы
      ├── spec/                 # глобальные стили (миксины, функции и переменные)
          ├── _autoload.scss/   # подключение внешних стилей (стили swiper)
          └── _reset.scss/      # сброс стилей
      └── main.scss/            # точка входа
  ├── public/                   # статика (картинки, иконки, шрифты)
      ├── images/               
      ├── fonts/                
      ├── icons/                # сборка из этой папки svg в sprite лист
      └── videos/               # webm, mkv, mp4, mov, wmv, flv, avi
  ├── views/                    # html/pug шаблоны
      ├── components/           # компоненты для pug
          └── mixins/           # миксины
              ├── icon.puп/     # встраивание иконок svg из sprite листа
              └── loop.pug/     # цикл (Нужна для упрощения верстки повторяющихся элементов)
      ├── layout/               # шаблоны страниц pug
      └── pages/                # страницы проекта (после добавления/удаления, перезапуск сборки)
  └── index.js/                 # подключение корневых файлов
  ```
