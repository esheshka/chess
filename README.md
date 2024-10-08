# chess

Мотивация задания: ссылка

За качество написания кода есть дополнительные баллы.

Гайд по стилю для начинающих разработчиков на Python: ссылка

  Реализовать программу, которая позволяет играть в шахматы. Взаимодействие с программой происходит через консоль. Игровое поле изображается в виде восьми текстовых строк и дополнительных строк с буквенным обозначением столбцов. Программа должна предоставлять пользователю возможность поочередно вводить ходы за белых и черных.

  Программа проверяет корректность ввода - допускаются только ходы, соответствующие правилам шахмат. Например, для пешки нужно реализовать следующие правила:
  
a) Пешка может ходить вперёд на свободное поле, расположенное непосредственно перед ней на той же самой вертикали.

b) С исходной позиции пешка может продвинуться на два поля по той же самой вертикали, если оба эти поля не заняты.

c) Пешка ходит на поле, занимаемое фигурой или пешкой противника, которая расположена по диагонали на смежной вертикали, одновременно забирая эту фигуру или пешку.


Более сложные правила ходов для пешек (взятие на проходе и превращение в фигуру) реализовывать не нужно.

  Проверять наличие мата и шаха не надо. Программа должна считать количество сделанных ходов. В случае ошибки в ответ на ввод пользователя выводится сообщение вида: «Error. Type: ХХХ.». Должны поддерживаться следующие типы ошибок:
• Wrong input format. – Для неправильного формата ввода хода.
• The piece cannot make the specified move. – Выбранная фигура не может сделать указанный ход, первая позиция в нотации не содержит фигуру, или содержит вражескую фигуру.


## Формат ввода

Программа взаимодействует со стандартным потоком ввода-вывода и управляется командами в консоли. В консоль передаются команды: draw и exit, или координаты хода в формате xi-zj, например e2-f3. Пользователь может вводить команды на любом шаге.


## Формат вывода

Перед каждым ходом программа должна вывести цвет фигур, которые должны ходить и номер их хода (например "white 1:")

Команда draw выводит в поток вывода изображение доски строго в нотации Рисунок 1. После вывода доски игра продолжается.

Команда exit завершает выполнение кода.


# Усложнение 1

Задание связано только с базовой частью. Это означает что в данной задаче не будет тестироваться функционал, реализуемый в других усложнениях базовой задачи.

Необходимо реализовать поддержку выполнения рокировки по всем шахматным правилам. Правила рокировки. Рокировка передается с помощью записи: 0-0 (короткая рокировка) или 0-0-0 (длинная рокировка). Каждая из сторон может сделать только одну рокировку в течение партии.


## Формат ввода

Программа взаимодействует со стандартным потоком ввода-вывода и управляется командами в консоли. В консоль передаются команды: draw и exit, или координаты хода в формате xi-zj, например e2-f3. Пользователь может вводить команды на любом шаге.


## Формат вывода

Команда draw выводит в поток вывода изображение доски строго в нотации Рисунок 1. После вывода доски игра продолжается.

Команда exit завершает выполнение кода.


# Усложнение 2

Задание связано только с базовой частью. Это означает что в данной задаче не будет тестироваться функционал, реализуемый в других усложнениях базовой задачи.

Реализовать возможность «отката» ходов. С помощью специальной команды можно возвращаться на ход (или заданное количество ходов) назад вплоть до начала партии: next_move; previous_move и next_move N; previous_move N (для перехода на несколько ходов). При необходимости возвращать ошибку типа: History out of bounds в формате «Error. Type: History out of bounds» - в случае, если следующего или прошлого хода нет. Если на отмотанном шаге сделан новый ход, то все шаги после удаляются и игра продолжается с этого хода.


## Формат ввода

Программа взаимодействует со стандартным потоком ввода-вывода и управляется командами в консоли. В консоль передаются команды: draw; exit; next_move; previous_move; next_move N; previous_move N, или координаты хода в формате xi-zj, например e2-f3. Пользователь может вводить команды на любом шаге.


## Формат вывода

Команда draw выводит в поток вывода изображение доски строго в нотации Рисунок 1. После вывода доски игра продолжается.

Команда exit завершает выполнение кода.


# Усложнение 3

Задание связано только с базовой частью. Это означает что в данной задаче не будет тестироваться функционал, реализуемый в других усложнениях базовой задачи.

Реализовать функцию подсказки выбора новой позиции фигуры: после выбора фигуры для хода функция подсказывает поля доступные для хода (формат ввода: координата и -) или фигуры соперника (с их позициями), доступные для взятия (формат ввода: координата), выбранной фигурой. Для короля этот функционал не обязателен.

Для подсказок полей доступных для хода и доступных для взятия вражеских фигур выводимые шахматные клетки необходимо отсортировать в алфавитном порядке (например "a6, b3, b5, d3, d5, e2, f1"). При попытке узнать возможные ходы фигуры противника - вывести сообщение как об отсутствии возможных ходов.

При реализации подсказок не нужно реализовывать подсказку хода "0-0" и "0-0-0", потому что эта задача не зависит от соответствующей задачи про рокировки.


## Формат ввода

Программа взаимодействует со стандартным потоком ввода-вывода и управляется командами в консоли. В консоль передаются команды: draw; exit; координаты хода в формате xi-zj, например e2-f3; координаты в формате xi- (для получения подсказок возможных ходов для этой фигуры), например a2-; координаты в формате xi (для получения списка вражеских фигур, которые можно забрать выбранной фигурой), например a2. Пользователь может вводить команды на любом шаге.


## Формат вывода

Команда draw выводит в поток вывода изображение доски строго в нотации Рисунок 1. После вывода доски игра продолжается.

Команда exit завершает выполнение кода.














