# redbutton

Данный скрипт состоит из простых команд, он превращает зашифрованные luks диски и разделы в бесполезные, удаляя luks заголовки и заменяет значения на рандомные в первой и во второй ячейке ключа Yubikey для работы Challenge response.
*Значения в ключе Yubikey меняются только если, ключ вставлен в USB порт.
*Чтобы восстановить доступ к зашифрованным дискам после инициализации скрипта, у вас должны быть резервные копии этих заголовков. Как сделать резервную копию заголовка написано в инструкции во вложении.

Инструкция по применению: копируете файлы в каталог /home/user/Redbutton, заходите в папку со скриптом, открываете в этой папке терминал, прописываете команду (без кавычек) "sudo chmod +x redbutton" и вводите root пароль, далее копируете ярлык "Red button.desktop" на рабочий стол и, если это необходимо, в параметрах ярлыка меняете путь до скрипта и параметры запуска.
В параметрах запуска ярлыка указана команда которая меняет раскладку клавиатуры на US, чтобы можно было ввести root пароль для запуска скрипта не задумываясь о текущей раскладке.

Тестировал на Manjaro Linux с окружением KDE. На дистрибутивах основанных на Debian также должно работать исправно.
Для работы скрипта может потребоваться установка дополнительных пакетов (xclip и sdmem).
