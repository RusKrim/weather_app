## Персональный проект по React

---

##### #1 Прогноз Погоды

![alt text](https://raw.githubusercontent.com/RusKrim/forecast_react_app/master/src/bus/forecast/assets/img/mockup.png "Weather App Mockup")

#####Техническое задание

Список функций которые реализовывать нужно обязательно

- Приложение должно уметь показывать погоду на 7 дней вперед

- Прогноз погоды должен отображать: день недели , число и месяц , температуру ,
  уовень влажности , вероятность дождя , а также тип дня ( Облачно , солнечно ,
  дождливо )
- По умолчанию выбирается погода на сегодня, но у пользователя есть возможность
  переключить день кликнув на другой день внизу страницы
- Приложение должно уметь фильтровать дни по заданым критериям. (Тип дня: облачно
  или дождливо, минимальная температура, максимальная температура)
- После применения фильтра приложение отображает только те дни которые
  удовлетворяют заданные критерии
- Если по заданным критериям нет доступных дней, нужно выводить текст По заданным
  критериям нет доступных дней
- Для работы со временем необходимо использовать библиотеку moment
- Приложение должно использовать данные с API

**Обратите внимание**

- Чекбоксы в фильтре работают как radio buttons, другими словами день может быть или
  облачным или солнечным
- Инпут в фильтре может принимать только числа
- Приложение показыват первым днем недели тот день который является текущим
- В случае применения фильтра максимальное количество дней для просмотра на
  экране должно быть не больше 7
- Если текущий фильтр отобрал больше чем 7 дней, то на экране нужно отображать
  ближайшие 7 дней
- Фильтр не показывает на экране погоду на предыдущие дни. Все дни которые были
  раньше сегодня считаются предыдущими.
- API сервер возвращает массив дней из которого нужно отфильтровать те дни которые
  нужны пользователю на экране

**Работа с API**

**URL адрес:** `http://api.backendless.com/520C1D14-9413-E1AA-FF78- 6A4DB0E26E00/9C9A66AC-959A-D6F4-FFAB-BD991AA34A00/data/forecast?pageSize=16`

**Метод:** GET

```bash
[
 {
 "rain_probability": 75, // вероятность дождя
 "humidity": 42, // уровень влажности
 "created": 1575270497746, // служебное поле, игнорируем
 "day": 1576447200000, // дата
 "updated": null, // служебное поле, игнорируем
 "objectId": "16A8399C-B0E5-9E8F-FF54-7E899F348B00", // уникальный
идентификатор
 "temperature": 19, // уровень температуры
 "type": "rainy", // тип дня, может быть: rainy или sunny или cloudy
 "ownerId": null, // служебное поле, игнорируем
 "___class": "forecast" // служебное поле, игнорируем
 }


```