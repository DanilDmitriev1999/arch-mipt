# Первое домашнее задание по курсу Архитектура ПО

## Запуск
`./start.sh`

## Метод GET
### Поиск по логину
`http://192.168.0.114/person?login=Violet_Flett5111@famism.biz`

Результат:

```
{
    "age": 47,
    "first_name": "Violet",
    "last_name": "Flett",
    "login": "Violet_Flett5111@famism.biz"
}
```


### Поиск по маске
`http://192.168.0.114/person?search&first_name=Am&last_name=A`

Рузльтат:

```[
    {
        "age": 36,
        "first_name": "Amelia",
        "last_name": "Allington",
        "login": "Amelia_Allington5563@grannar.com"
    },
    {
        "age": 73,
        "first_name": "Amelia",
        "last_name": "Avery",
        "login": "Amelia_Avery4374@muall.tech"
    }
]
```
## Метод POST
```
url = '192.168.0.114/person'
data = {'login': 'danildmitrievv11@gmail.com',
        'first_name': 'Danil',
        'last_name': 'Dmitriev',
        'age': 22}

r = requests.post(url, data=json.dumps(payload))
```
Результат:
```
{
    "result": true
}
```

### Проверим по логину:
`192.168.0.114/person?login=danildmitrievv11@gmail.com`

Результат:
```
{
    "age": 22,
    "first_name": "Danil",
    "last_name": "Dmitriev",
    "login": "danildmitrievv11@gmail.com"
}
```


