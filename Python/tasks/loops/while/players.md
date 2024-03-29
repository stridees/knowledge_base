Для игры в "Поле Чудес" случайным образом сформирована тройка игроков: Заяц, Волк, Колобок

Реализуйте программу с _текстовым меню_, которая позволит выполнять операции по удалению и замене игроков.

После запуска программы отображается меню с описанием доступных команд (`просмотреть`, `заменить`, `удалить` и `выход`). Пользователь вводит название команды и необходимые данные, команда выполняется. 

После успешного выполнения команды предлагается ввести еще одну команду. Программа завершается после ввода команды `выход` либо когда в списке остался только один игрок (остальные были удалены).

После выполнения каждой операции необходимо выводить текущее количество игроков.

Гарантируется, что при вводе команды пользователь будет набирать только одно из четырех указанных слов.  
При вводе количества игроков будет набирать только числа от 1 до 3.

---

_Пример 1_

> МЕНЮ (доступные команды):  
> \- "просмотреть", чтобы просмотреть имя игрока  
> \- "заменить", чтобы заменить игрока  
> \- "удалить", чтобы удалить игрока  
> \- "выход", чтобы выйти

> Введите команду: **просмотреть**  
> Введите номер игрока (от 1 до 3): **1**  
> Под номером 1 играет Заяц  
> Число игроков составляет 3

> Введите команду: **заменить**  
> Введите номер игрока (от 1 до 3): **1**  
> На кого необходимо заменить: **Медведь**  
> Игрок Медведь заменяет игрока Заяц!  
> Число игроков составляет 3
>
> Введите команду: **просмотреть**  
> Введите номер игрока: 1  
> Под номером 1 играет Медведь  
> Число игроков составляет 3
>
> Введите команду: **выход**  
> Программа завершена. До новых встреч! 

<br>

_Пример 2_

> _<Вывести меню с описанием команд (см. Пример 1)>_
> 
> Введите команду: **удалить**  
> Введите номер игрока: **2**  
> Удаляется игрок Волк...  
> Число игроков составляет 2  
>
> Введите команду: **просмотреть**  
> Введите номер игрока (от 1 до 2): **2**  
> Под номером 2 играет Колобок  
> Число игроков составляет 2

> Введите команду: **выход**  
> Программа завершена. До новых встреч! 

<br>

_Пример 3_

> _<Вывести меню с описанием команд (см. Пример 1)>_
> 
> Введите команду: **удалить**  
> Введите номер игрока: **3**  
> Удаляется игрок Волк...  
> Число игроков составляет 2  
>
> Введите команду: **удалить**  
> Введите номер игрока (от 1 до 2): **2**  
> Удаляется игрок Колобок...  
>
> В списке остался единственный игрок
>
> Программа завершена. До новых встреч!
