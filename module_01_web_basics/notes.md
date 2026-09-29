
Web4

- Комментариев вернулось: 5
- С postId = 5: 5

Web5

- Объектов: 3
- id: 1, 2, 3

Web6

- postId=3 - 5
- postId=4 - 5
- Параметр postId: фильтрует комментарии по номеру поста.

Web7

- Гипотеза: _limit ограничивает количество объектов в ответе указанным числом.
- _limit=2 - 2
- _limit=7 - 7

Web8

https://jsonplaceholder.typicode.com/comments?postId=7&_limit=4

Часть Значение
Схема https 
Хост jsonplaceholder.typicode.com
Порт не написан, подразумевается 443
Путь /comments
Query postId=7, _limit=4

http://localhost:8080/tasks?page=2&sort=date

Часть Значение 
Схема http
Хост localhost
Порт 8080
Путь /tasks
Query page=2, sort=date

https://api.example.com:3000/users/42/posts?status=active

Часть Значение
Схема https
Хост api.example.com
Порт 3000 |
Путь /users/42/posts
Query status=active

Web9

/users/2/posts - объектов: 10, id первого: 11
/posts?userId=2 - объектов: 10, id первого: 11
Вывод: данные одни и те же.

Web10

/users/1 - 200
/users/11 - 404
/users/1?foo=bar - 200
Вывод: ресурс ломает путь, query на ресурс не влияет.

Web11

- Content-Type ответа /users: application/json; charset=utf-8
- Content-Length ответа /users: 1847
- Content-Type HTML-страницы: text/html; charset=utf-8



Web12

- _page=1 - объектов: 5, id первого: 1
- _page=2 - объектов: 5, id первого: 6
- Параметр _page: выбирает номер страницы.

