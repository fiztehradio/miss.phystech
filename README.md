# Выбери свою мисс мипт! 

В этом репозитории ты сможешь найти формальные правила участия, несколько идей, а также датасеты, которые могут пригодиться при построении моделей. Вот в [этой таблице](https://docs.google.com/spreadsheets/d/1-UxzpI56aBR5tyWkn3LJC7Qlamm4IIj-29WbIHz-I_c/edit#gid=1854006318) ты также можешь найти полный список участниц и их награды. Пишите нам в [группу VK](https://vk.com/radiomipt), если вы хотите дополнить данные.

## Задание
Разработай **ИССКУСТВЕННЫЙ ИНТЕЛЛЕКТ**, который выберет **СВОЮ МИСС МИПТ**, и пришли его нам! Именно не "предскажет победительницу", а определит победительницу сам. По каким критериям выбирать - решать вам! 

Перед самым финалом, мы
* Прогоним все присланные алгоритмы на новый участницах, 
* Усредним результаты,
* Выберем **ТУ САМУЮ** и 
* Наградим в специальной номинации.

## Формальные требования 
* Код алгоритма должен быть загружен в публичный репозиторий на GitHub / Gitlab, а ссылка на него прислана в группу [Физтех.Радио в VK](https://vk.com/radiomipt).
* В репозитории должно быть указано:
  * В каком формате подавать вашему алгоритму данные на вход,
  * Поверхностное описание вашего алгоритма,
  * Как получить и интерпретировать выходные результаты вашего алгоритма.
* Если алгоритм подразумевает некое "обучение", в репозитории должна быть выложена уже обученная модель.
* Если ваш алгоритм использует какие-нибудь сторонние данные, в ваш репозиторий должен быть загружен скрипт, который позволит нам выкачать необходимые данные о будущей участнице. 
* Если ваш алгоритм подразумевает нарушение одного из вышеперечисленных пунктов, просьба связаться с [организаторами](https://vk.com/radiomipt).

## Примеры алгоритмов

### Определю лучшую по фотографии
Есть фотографии участниц с отбора, есть победительницы прошлых лет. Все просто.
<img src="https://user-images.githubusercontent.com/5613295/53300004-de538500-3852-11e9-9f76-1fa758961ccd.png" width="300" height="250">

Вы обучили сеточку, которая просто выдает вероятность победы участницы с данным фото. В репозиторий вы выложили обученную модель, указали, как можно подать ей на вход фотографию и как интерпретировать выходные данные.

Жюри скачает фотографии участниц с отбора, прогонит их всех через вашу модель, усреднит результаты для одной участницы, если будет больше одной фотки.

### Instagram to win them all
Допустим, ваша команда аналитиков выявила закономерность: чем круче Instagram профиль конкурсантки, тем больше она достойна победы в конкурсе. При этом вы солидарны с жюри прошлых лет и обучили свою модель на прошлогодних победительницах.

В итоге вы разработали алгоритм, который 
* На вход получает *Instagram username* конкурсантки
* На выходе выдает число, которое определяет вероятность победы участницы с этим инстаграмм профилем
* В описании алгоритма вы указали, какую веростность проставлять тем участницам, у которых нет инстаграмм аккаунта или у которых профиль закрытый.
* Так как ваша метрика "крутости инстаграм профиля" использует данные о подписчиках профиля, вы указали, что необходимо будет спарсить актуальные данные и положить их в такую-то папку в таком-то формате.

После оглашения списка всех участниц, жюри самостоятельно прогонит через ваш алгоритм профили всех участниц, соберет вероятности и добавит их итоговую смесь результатов всех алгоритмов.
