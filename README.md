# directum-cluster-playbook

ИСПОЛЬЗОВАТЬ ТОЛЬКО ДЛЯ РАЗВОРАЧИВАНИЯ СИСТЕМЫ НА ASTRA LINUX

Данный плейбук расчитан на то, что система будет стоять в локальной сети ЗА прокси сервером и принимать https снаружи, а http внутри
Перед запуском данного плейбука выполните:

0) git clone https://github.com/paperdadfo/directum-cluster-playbook.git

1) На входящем прокси сервере настройте запись запись вида:
test.rx.compony.name -> [balancer]

2) Отредактируйте файл hosts.txt на свое усмотрение

3) убедитесь что у вас на всех развернутых серверах один пользователь и один пароль, а так же настроен SUDO без использования пароля.

Протестирована работа на машине с установленным:

python version = 3.10

ansible [core 2.12.2]



П.С
Из ~ 100 пробных запусков данного плейбука с астра линуксом возникали абсолютно рандомные ошибки
Пример это ошибка невозможности найти пакет APT или модуль APT.
В данном случае помогает перезапустить плейбук.
В среднем эта ошибка воспроизводиться в 1 из ~12 запусков.
Примерно это все может возникать из-за python 3.5 на астра линукс.

На других ОС данных особенностей замечено не было (но данный плейбук без модернизации использовать невозможно).
