# Image Router

Простой маршрутизатор для отображения изображений на основе цифр в URL.

## Описание

**Image Router** - это небольшой HTML/JavaScript инструмент, который парсит URL, извлекает из него цифры и показывает соответствующее изображение. Может использоваться как `src` для тега `<img>`.

## Использование

### Базовый пример

```html
<img src="https://dns-fw.github.io/image-router/image-router.html#123" alt="Image">
```

### Как это работает

1. Инструмент берёт последнюю цифру из URL (в примере выше это `3`)
2. 2. На основе этой цифры (от 0 до 9) отображает соответствующее изображение
   3. 3. Каждой цифре соответствует одно изображение
     
      4. ### Примеры URL
     
      5. - `.../image-router.html/0` - показывает изображение для цифры 0
         - - `.../image-router.html/1` - показывает изображение для цифры 1
           - - `.../image-router.html/123` - показывает изображение для цифры 3
             - - `.../image-router.html/abc456` - показывает изображение для цифры 6
              
               - ## Настройка изображений
              
               - Отредактируйте файл `image-router.html` и измените объект `imageMap` на строку 28:
              
               - ```javascript
                 const imageMap = {
                     0: 'https://ваш-url-изображения-0.jpg',
                     1: 'https://ваш-url-изображения-1.jpg',
                     // ... и так далее для цифр 2-9
                 };
                 ```

                 ## Особенности

                 ✅ Работает как `src` для `<img>` тегов
                 ✅ Поддерживает все современные браузеры
                 ✅ Автоматически обрабатывает ошибки
                 ✅ Лёгко настраивается для любых URL изображений

                 ## Примеры использования

                 ### В HTML

                 ```html
                 <img src="https://dns-fw.github.io/image-router/image-router.html/5" alt="Product 5">
                 ```

                 ### Динамически на JavaScript

                 ```javascript
                 const imageId = 3;
                 const img = document.createElement('img');
                 img.src = `https://dns-fw.github.io/image-router/image-router.html/${imageId}`;
                 document.body.appendChild(img);
                 ```

                 ## Лицензия

                 MIT
