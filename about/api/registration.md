# Registration
#### For registrate user we need to send this fields
- `f_name - string [required]`
- `name - string [required]`
- `l_name - string [required]`
- `teip - int [required]`
- `born - string [required]`
- `tpl_tree_number - int [required]`
- `phone - string [required]`
- `email - string [required]`
- `password1 - string [required]`
- `password2 - string [required]`
- `submit - string [required]`
- `gender - string [required]`

## f_name
* Фамилия пользователя

## name
* имя

## l_name
* Отчество

## teip 
* id тейпа пользователя который он выберет на странице регистрации
  во вкладке **Дополнительная информация** но человека когда он 
  нажмет на Поле **Тейп** то выподает меню для выбора своего тейпа

## born
* Это поле является датой рождения и я должен его отправлять именно в током
  формате `год-месяц-день` 

## tpl_tree_number
* когда ему показывается список со всеми совпадениями в дереве, то в этом поле мы отправляем id человека. Это такое
временное поле, после того как его личность будет подтверждена, это значение переносится в поле tree_number

## phone
* Телефон номер пользователя на который отправится смс с кодом потверждения
  подерживаемые номера это (RU)
* Есть ли у номера ограниченная длина? , желательно прислать в формате 79999999999,
но в любом случае я на стороне сервера убираю из номера все лишние символы и привожу к нужному
мне формату 

## email
* почта пользователя является основным полем для входа

## password1
* пароль

## password2
* пароль2 не лучше было бы удалить это поле ? Я буду и так проверять
  совпадение пароля со стороны пользователя. И не будем делать лишних
  запросов на сервер если пароль не совпадает
  лучше прислать все же, потому что:
  1. у меня это проверка уже реализована
  2. лучше перепроверять на случай если что-то пойдет не так

## submit
* Не знаю для чего это поле
  это старое поле, можно его не отправлять

## gender
* Пол пользователя, на даный момент его нету надо его добавить
  это поле добавлю 


# Логика регистрации
Человек заходит на экран регистрации на первом экране он заполняет
*Фамилия имя отчество после Тейп пол Дата рож*
Затем нажимает на кнопку далее.
Его перебрасывает на второй экран где он заполняет поля
*Email Phone password1 password2*
Нажимает на кнопку принять соглашения и жмет кнопку 
**Зарегистрироваться**
После выползает снизу виджет для потверждения телефона через смс код
Он пишит свой код и нажимает на кнопку подтвердить 
после этого ему подгружается список всех совпадений в БД по его ФИО, 
он выбирает в списке себя и id выбора уже помешается в поле tpl_tree_number
если нет совпадений, то присылаешь просто -1 в поле tpl_tree_number









