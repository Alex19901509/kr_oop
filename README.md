# KR_OOP
В этом проекте я написал интеграцию с внешним сервисом.

Написал программу, которая будет получать информацию о вакансиях с платформы hh.ru в России, сохранять ее в файл и позволять удобно работать с ней: добавлять, фильтровать, удалять.

Реализация:
Создал абстрактный класс для работы с API сервиса с вакансиями. Реализовал класс, наследующийся от абстрактного класса, для работы с платформой hh.ru. Класс умеет подключаться к API и получать вакансии.
Создал класс для работы с вакансиями. В этом классе следующие атрибуты: название вакансии, ссылка на вакансию, зарплата, требования. Класс поддерживает методы сравнения вакансий между собой по зарплате и валидирует данными, которыми инициализируются его атрибуты.
Способ валидации данных - быть проверка, указана или нет зарплата. В этом случае выставляется значение зарплаты 0.

Определил абстрактный класс, который обязывает реализовать методы для добавления вакансий в файл, получать данные из файла по указанным критериям и удалять информации о вакансиях. Создал класс для сохранения информации о вакансиях в JSON-файл.
Данный класс выступает в роли основы для коннектора, заменяя который, можно использовать в качестве хранилища одну из баз данных или удаленное хранилище со своей специфической системой обращений.

Создал функцию для взаимодействия с пользователем. Функция взаимодействует с пользователем через консоль. Возможности этой функции:
ввести поисковый запрос для запроса вакансий из hh.ru;
получить топ N вакансий по зарплате (N запрашивать у пользователя);
получить вакансии с ключевым словом в описании.