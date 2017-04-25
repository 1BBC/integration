# П'ЯТЕ ПОКОЛІННЯ ІНТЕГРАЦІЇ!

### Початок інтеграції

Закинь файли **api.php** та **api.js** в корінь (Туди де лежить index.html).

Відкрий api.php та зміни 4 значення: _offer_id_, _country_, _api_key_, _user_id_ (Ти їх можеш знайти в особистому кабінеті тери), за потребою можна вказати стрім - поле '_stream_id_'.

Відкрий index.html, знайди форму <form> та задай значення її атрибута id як "form1" (id="form1"), якщо атрибута id немає - створи його, якщо такий атрибут вже існує, наприклад id="model-form", то зміни model-form на form1.
	
	Примітка:	Задавати формі два ідентифікатори не можна! В такому випадку їй буде присвоєно перший ідентифікатор і інтеграція може не запрацювати.

Якщо на сторінці дві форми, то для другої інкрементуй ідентифікатор - id="form2"

Після цих дій форма має набути вигляду <form class="деякі класи" method="post" action="деяке значення" id="form1 або form2>

Далі, в цьому ж index.html, перед закриваючим теґом </body> додай наступний скрипт. Цей скрипт задасть правильне значення атрибута action, зробить поля обов'язковими, встановить потрібний петод передачі форми і при наявності відправить в трекер utm мітки.

```html
<script src="api.js"></script>
```


На цьому інтеграцію завершено. Можеш відправляти тестову заявку. Якщо все пройшло добре - тебе має перенаправити на success.html та в кореневій директорії буде створено папку log. Після відправлення тестової заявки, зайди в неї відкрий новостворений лог-файл і перевір чи потрапита в нього заявка.

	Порада:		Якщо на сторінці дві форми, обо'язково перевіряй другу форму!

	Порада: 	Більш детально про форму та її атрибути можеш прочитати за посиланням - https://css.in.ua/html/tag/form

	Примітка:	Якщо ти вже інтегрований по попередніх поколіннях - нічого страшного, все буде працювати, але в подальшому використовуй друге покаління.

	Примітка:	якщо у тебе виникли питання чи побажання - ім'я моє Володимир - скайп nagard11


### Зміни в поколіннях:

    - Перше поколіннях      - Раніше інтеграції використовували бібліотеку jquery, не на всіх сторінках вона підключена. Також вона могла бути підключена в різних місцях, що створювало вагомий дискомфорт.

    - Друге покоління       - більше не використовує jquery. Також було додано примусове просвоєння значення для атрибута method (method="post")

    - Третє покоління       - виправлено помилку, коли я просив призначити формі не правильний ідентифікатор.

    - Четверте покоління    - Тепер в ґет параметрах передаються: sub_id, sub_id_1, sub_id_2, sub_id_3, sub_id_4 (Через ці параметри можеш передавати в теру слік_ід та інші речі).

    - П'яте покоління       - Тепер немає неохідності створювати папку log, це буде зроблено автомачично.
                            - Поля ім'я та телефон тепер обов'язкові, перевірка їх є як на клієнстській стороні, так і на серверній.
                            - Js сценарій винесено в окремий файл. Д
                            - Тепер можна вказати стрім
                            
    - Шосте покоління       - Завдяки допомозі Максима Бражніка, тепер не потрібно присвоювати жодних ідентифікаторів формам. Скрипт сам знайде всі форми і зробить все, що потрібно.


