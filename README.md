# Compiled-TCP-congestion-control-PCC-without-errors
Ready binary file Tcp Congestion Control Compiled without errors

I have compiled "without errors" on Devuan 4 (Debian 11) TCP Control PCC that operates on the basis of losses.
The source code is taken from.
https://github.com/KaiwenZha/PCC-Vivace
Maybe someone will come in handy.

Installation.
Only Debian.
If you want to use it on other "Distributions", you will have to compile it yourself.
Download tcp_pcc.ko or archive with it.
Unpack.
sudo cp tcp_pcc.ko /lib/modules/$(uname -r)/kernel/net/ipv4
sudo depmod -a

You can without rebooting, immediately activate.
sudo gedit /etc/sysctl.conf
At the very end, add to the new line.
net.ipv4.tcp_congestion_control = pcc
Apply.
sudo sysctl -p
Verify.
sudo sysctl -a | grep pcc

Compile PCC Latency Without errors, it did not work


Скомпилированный мною "Без Ошибок" на Devuan 4(Debian 11) TCP congestion control PCC который работает на основе Потерь(Loss).
Исходный код взят из.
https://github.com/KaiwenZha/PCC-Vivace
Может кому-то пригодится.

Установка.
Только для Debian.
Если хотите использовать на других "Дистрибутивах", то прийдется компилировать самостоятельно.
Скачать tcp_pcc.ko или архив с ним.
Распаковать.
sudo cp tcp_pcc.ko /lib/modules/$(uname -r)/kernel/net/ipv4
sudo depmod -a

Можно без перезагрузки, сразу активировать.
sudo gedit /etc/sysctl.conf
в самый конец, в новой строке добавить.
net.ipv4.tcp_congestion_control = pcc
Применить.
sudo sysctl -p
Проверить.
sudo sysctl -a | grep pcc

Скомпилировать PCC Latency Без ошибок Не получилось.
