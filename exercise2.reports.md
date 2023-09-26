## Баг-репорты: 

### Баг-репорт №1. Код ответа 502 на запрос GET https://sbermegamarketru.webim.ru/button.php при обновлении главной страницы https://sbermegamarket.ru/

 **Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Обновить страницу https://sbermegamarket.ru/
 - Проверить корректность ответа на выполненный запрос во вкладке "Console" в DevTools

 **Ожидаемый результат:** 
 - HTTP статус: 200 ОК, отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  

 - HTTP статус: 502 (Bad Gateway) на запрос GET https://sbermegamarketru.webim.ru/button.php . Указывает на неправильную работу прокси-сервера, DNS-сервера и сервера, на котором размещен сайт.
 
 **Серьезность:** Minor 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)

### Баг-репорт №2. Ошибка ```TypeError: DDManager Custom Event "Viewed Product Listing" Error``` при открытии "Условия использования сайта" в футере страницы

 **Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Нажать на "Условия использования сайта" в футере страницы https://sbermegamarket.ru/
 - Проверить отсутствие ошибок во вкладке "Console" в DevTools

 **Ожидаемый результат:** 
 - Отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  

 - ```TypeError: DDManager Custom Event "Viewed Product Listing" Error```

 **Серьезность:** Minor 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)

### Баг-репорт №3. Код ответа 400 на запрос авторизации GET https://id.sber.ru/CSAFront/api/userdata?client_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a

 **Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Нажать на иконку авторизации по СберID
 - Проверить корректность ответа на выполненный запрос во вкладке "Console" в DevTools

 **Ожидаемый результат:** 
 - HTTP статус: 200 ОК, отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  
 - HTTP статус: 400 Bad Request на запрос GET https://id.sber.ru/CSAFront/api/userdata?client_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a
 
 **Серьезность:** Minor 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)

### Баг-репорт №4. Код ответа 404 на запрос POST https://stream.datago.ru/mp/collect?tid=UA-89387429-1 при переходе в раздел "Супермаркет"

**Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Нажать на баннер "Супермаркет" в хэдере страницы https://sbermegamarket.ru/
 - Проверить корректность ответа на выполненный запрос во вкладке "Console" в DevTools

 **Ожидаемый результат:** 
 - HTTP статус: 200 ОК, отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  
 - HTTP статус: 404 Not Found на запрос POST https://stream.datago.ru/mp/collect?tid=UA-89387429-1

**Серьезность:** Minor 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)

### Баг-репорт №5. Ошибка ```Ошибка закрытия сессии в mgate-client``` на запрос перехода на VK.com

**Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Нажать на иконку "VK" в футере страницы https://sbermegamarket.ru/
 - Проверить корректность ответа на выполненный запрос во вкладке "Console" в DevTools

 **Ожидаемый результат:** 
 - HTTP статус: 200 ОК, отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  
 - HTTP статус: ```Ошибка закрытия сессии в mgate-client node_modules.3f638be7.js:2:383012``` 

**Серьезность:** Minor 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)

### Баг-репорт №6. Ошибка ``` net::ERR_FAILED 200 ``` неуспешная отправка GET-запроса на VK.com

**Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Открыть меню "Маркетплейс" в футере страницы https://sbermegamarket.ru/ и нажать на раздел меню "Настоящий маркетплейс"
 - Проверить отсутствие ошибок во вкладке "Console" в DevTools
   
 **Ожидаемый результат:** 

 - отсутствие ошибок во вкладке "Console" в DevTools

 **Фактический результат:**  

 - GET https://vk.com/rtrg?p=VK-RTRG-1421183-77G99&products_event=view_other&price_list_id=1&e=1&i=0&metatag_url=%2F%2Fsbermegamarket.ru%2Finfo%2Fabout-sbermegamarket-ru%2F&metatag_title=%D0%9E%20%D0%BA%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D0%B8%20-%20%D0%9C%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%20SberMegaMarket.ru ```net::ERR_FAILED 200```

**Серьезность:** Minor 

 ### Баг-репорт №7. Ошибка 404 "Страница не найдена" при переходе в раздел "Красота"

**Предшествующие условия:** 
 - открыт сайт [СберМегаМаркета](https://sbermegamarket.ru/) в браузере Firefox
 - открыта вкладка "Console" в DevTools

 **Шаги воспроизведения:**
 - Нажать на баннер "Красота" в хэдере страницы https://sbermegamarket.ru/
 - Проверить корректность отображения данных выбранного раздела   

 **Ожидаемый результат:** 
 - Открывается раздел "Красота" с соответствующей данному разделу информацией

 **Фактический результат:**  
 - изображение баннера с ошибкой 404 "Страница не найдена"

**Серьезность:** Major 

 **Окружение** ОС - macOS Ventura 13.3.1 (a) (22E772610a), Firefox Browser версия 115.0 (64-разрядный)



 