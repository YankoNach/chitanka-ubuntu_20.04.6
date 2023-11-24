# chitanka-ubuntu_20.04.6
Моят доста скромен (и вероятно - некадърен) опит за chitanka на виртуална машина
Това е chitanka на на VirtualBox виртуална машина Ubuntu 20.04.6 LTS - (Focal Fossa). Актуална е за съдържанието на chitanka.info към 19.11.2023 г. 
Създадена е с помощта на chitanka-installer от https://github.com/chitanka/chitanka-installer
Параметрите на "образа" са:
 - Oracle VirtualBox Версия 7.0.8 r156879 (Qt5.15.2) (може да бъде свален на https://www.virtualbox.org/wiki/Downloads - за Windows; MacOs; множество Linux distro's; Solaris; etc...)
 - Настройките на виртуалната машина (ВМ) RAM 1024 Mb; 2 processor's cores; hard-disk 55 Gb; videoRAM 32 Mb;  NO hardware video acceleration ...
 - ВМ използва "Мостов адаптер" или на En: "Bridged network" - тук, евентуално трябва да изберете основния си мрежов интерфейс - било Ethenet или безжичен (за ВМ той винаги е Ethernet  и е свързан)
 - ВМ автоматично се логва като потребител chitanka ; с парола 3.14159
 - Потребител chitanka има sudo права, т.е. ако искате да изпълните команда като root, просто пишете sudo [командата, която искате да изпълните като root] + ENTER ... Въвеждате паролата на потребител chitanka: "3.14159" (без кавичките :-)
   Сървърите за ъпдейт на ВМ са конфигурирани за българско "огледало"... Ако сте в чужбина и достъпът до български сървъри е бавен, то можете да конфигурирате "огледалото" за международен достъп така:
   sudo cp /etc/apt/sources.list /etc/apt/sources.list.bg
   sudo rm /etc/apt/sources.list
   sudo cp /etc/apt/sources.list.international /etc/apt/sources.list
ВАЖНО!
За да можете да се свържете с локалната "chitanka" било от хоста (машината, на която е инсталиран VirtualBox и на която работи читанката), било от машина (лаптоп, таблет или телефон) в локалната ви мрежа, трабва да знаете IP адреса на виртуалната читанка! 
Това става с командата от терминала на ВМ:
hostname -I (тук I е главно "i" - английското "Ай" - като за Аз!
Може и с командата ifconfig , но тогава отговорът е малко по-сложен, трябва да се търси какво има непосредствено след "inet" полето в записа за основния мрежов адаптер, НЕ "lo" !
След това въведете в полето за адрес на браузера си нещо като http://192.168.xxx.xxx (заменете ххх с правилните цифри получени по-горе)
Ако имате бележки или въпроси - чувствайте се свободни да ме питате или попържате на khankrum359@gmail.com
