# redbutton
RU: Простой скрипт на случай если вам нужно срочно сделать ваши luks зашифрованные диски бесполезными и изменить значения в слотах Challenge responce ключа Yubikey.
EN: It's a simple script in case you need to urgently make your luks encrypted disks useless and change the values in the Challenge responce slots of the Yubikey.

# Назначение/Purpose
RU: Данный скрипт предназначен для людей для которых недостаточно иметь luks зашифрованные разделы для того чтобы чувствовать что информация в безопасности. 

EN: This script is designed for people for whom it is not enough to have luks encrypted partitions to feel that the information is safe.

# Описание/Description
RU: Данный скрипт состоит из простых команд, он превращает зашифрованные luks диски и разделы в бесполезные, удаляя luks заголовки и заменяет значения на рандомные в первой и во второй ячейке ключа Yubikey для работы Challenge response.
-Значения в ключе Yubikey меняются только если, ключ вставлен в USB порт.
-Чтобы восстановить доступ к зашифрованным дискам после инициализации скрипта, у вас должны быть резервные копии этих заголовков. Как сделать резервную копию заголовка написано в инструкции.

EN: This script consists of simple commands, it turns encrypted luks disks and partitions into useless ones by removing the luks headers and replacing values with random values in the first and second cells of the Yubikey key to make the Challenge response work.
*The values in the Yubikey key only change if the key is inserted into the USB port.
*In order to restore access to the encrypted disks after the script has been initialized, you must have backups of these headers. How to back up the header is written in the instructions.

# Установка/Installation
RU: Копируете файлы в каталог /home/user/Redbutton, заходите в папку со скриптом, открываете в этой папке терминал, прописываете команду (без кавычек) "sudo chmod +x redbutton" и вводите root пароль, далее копируете ярлык "Red button.desktop" на рабочий стол и, если это необходимо, в параметрах ярлыка меняете путь до скрипта и параметры запуска.
В параметрах запуска ярлыка указана команда которая меняет раскладку клавиатуры на US, это сделано чтобы вы могли ввести root пароль для запуска скрипта не задумываясь о текущей раскладке.

EN: Copy the files to the directory /home/user/Redbutton, go to the folder with the script, open a terminal in this folder, type the command (without quotes) "sudo chmod +x redbutton" and enter the root password, then copy the shortcut "Red button.desktop" to the desktop and, if necessary, in the parameters of the shortcut change the path to the script and launch parameters.
In the parameters of the shortcut there is a command that changes the keyboard layout to US, this is done so you can enter the root password to run the script without thinking about the current layout.

# Тестирование/Tests
RU: Скрипт тестировался на Manjaro Linux с окружением KDE. На дистрибутивах основанных на Debian также должно работать корректно.
Для работы скрипта может потребоваться установка дополнительных пакетов (xclip и sdmem).

EN: The script was tested on Manjaro Linux with KDE environment. On distributions based on Debian should also work correctly.
You may need to install additional packages (xclip and sdmem) to make the script work.

# ВАЖНО/Attention
RU: Не запускайте скрипт если у вас нет резервных копий luks заголовков и кодов Challenge response. Лучше всего тестировать скрипт на виртуальной машине. Перед тестированием скрипта на основной системе подумайте трижды о том, как вы будете всё восстанавливать.

EN: Do not run the script if you do not have backups of luks headers and Challenge response codes. It is best to test the script on a virtual machine. Before testing the script on a host system, think three times about how you will restore everything.
