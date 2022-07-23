{
    "current_page": 1,                     -> int : not null
    "first_page_url": "link",              -> str : not null
    "from": 1,                             -> str : null
    "last_page": 85,                       -> int : not null
    "last_page_url": "link",               -> str : not null
    "next_page_url": "link",               -> str : null
    "path": "link",                        -> str : not null
    "per_page": 20,                        -> int : not null
    "prev_page_url": null,                 -> str : null
    "to": 20,                              -> int : null
    "total": 1692                          -> int : not null
    "data": [
        {
            "profile_photo_path": null,    -> str : null
            "id": 11,                      -> int : not null
            "fio": "Салтамак Ужахов",      -> str : not null
            "born": "2020-08-21",          -> str : null
            "die": null,                   -> str : null
            "father_id": 10,               -> int : null
            "teip": 103,                   -> int : null
            "father_fio": "Ужах",          -> str : null
            "teip_title": null             -> str : null
        },
    ],
} 


# If in data we have nothing i reseave the data field like this
{
  ....
  "data": []
}


### "teip"
* int : null
* может ли teip быть null если fio не будет null? 
* И teip это и есть tpl_tree_number который я должен отправлять при регистрации?

### "teip_title"
* Это имя тейпа да? типо ужаховы оздоевы и т.д



### [!] Всегда возвращать мне такую модель при каждом запросе где есть пагинация
