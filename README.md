Forms for WordPress by Systemo
=========================

Плагин позволяет генерировать форму за счет шорткодов. Сохраняя данные в посты типа Сообщение и отправляя на эл почту.


# Шорткоды
## [form_cp]
Шорткод, который генерирует обертку формы. Включает в себя типовые атрибуты тега form в HTML
Внутрь этого шорткода помещаются шорткоды полей.

Дополнительные атрибуты:
spam_protect=1 - включает защиту от спама по клику
form_name='Имя формы' - имя формы, которое затем идет в заголове сообщений, как при сохранении в консоли, так и при отправлении на почту

## [input-cp]
Шорткод поля ввода. Аналогичен тегу input в HTML.

# Примеры
## Пример #1 - Простая форма и метод GET

[form-cp method="GET" id="myform"]

[input-cp type=text label=text name="text"]

[input-cp type=submit value="Отправить" name="submit"]

[/form-cp]


## Пример #2 - форма обратной связи

[form-cp name_form='Сайт под ключ - заявка' spam_protect=1 id="myform"]

[input-cp type=text name="name" placeholder="Имя" meta="Имя"]

[input-cp type=text name="tel" placeholder="Телефон" meta="Телефон"]

[input-cp type=email name="email" placeholder="Электронная почта" required="true" meta="Электронная почта"]

[textarea-cp placeholder=Комментарий name="comment" meta="Комментарий"]

[input-cp type=submit class="btn btn-success" value="Отправить" name="submit"]

[/form-cp]
