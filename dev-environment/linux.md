# Некоторые простые команды

```bash
macbook:~ vitalij$ docker run -it ubuntu bash

root@8badb90a35b9:~# date
Wed Jun 6 18:01:37 UTC 2018
```

date выводит текущие время и дату

df объем свободного пространства на дисках

free объем свободного пространства в памяти

```
root@8badb90a35b9:~# df
Filesystem     1K-blocks    Used Available Use% Mounted on
overlay         61255492 1191248  56922920   3% /
tmpfs              65536       0     65536   0% /dev
tmpfs            1023468       0   1023468   0% /sys/fs/cgroup
/dev/sda1       61255492 1191248  56922920   3% /etc/hosts
shm                65536       0     65536   0% /dev/shm
tmpfs            1023468       0   1023468   0% /sys/firmware

root@8badb90a35b9:~# free
              total        used        free      shared  buff/cache   available
Mem:        2046940      212196      463332         664     1371412     1676500
Swap:       1048572           0     1048572
```

Первое,. что. мы. попробуем. изучить. \(после. пробных. нажатий. на. клавиши\),. —. .навигацию. в. файловой. системе. Linux.. В. этой. главе. введем. в. обиход. следующие. команды:

.pwd.—.выводит.название.текущего.рабочего.каталога..

cd.—.выполняет.переход.в.другой.каталог.

.ls.—.выводит.список.содержимого.каталога.

```
root@8badb90a35b9:/# pwd
/
root@8badb90a35b9:/# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
boot  etc  lib   media  opt  root  sbin  sys  usr

root@8badb90a35b9:/# cd /home/    
root@8badb90a35b9:/home# 

root@8badb90a35b9:/home# cd ..
root@8badb90a35b9:/# 
```

cd Сменить рабочий каталог на домашний  
cd - Сменить рабочий каталог на предыдущий рабочий каталог  
cd ~username Сменить рабочий каталог на домашний каталог пользователя username.



.ls.—.выводит.список.содержимого.каталога..

file.—.определяет.тип.файла.  
.less.—.выводит.содержимое.файла.

ls 

Команде.можно.явно.указать.каталог,.содержимое.которого.требуется.вывести и.даже.несколько.каталогов..

Можно.также.изменить.формат.вывода,.чтобы.получить.больше.информации:

Параметр.-l,.добавленный.в.команду,.требует.использования.«длинного».\(long\). формата.вывода.параметр.t,.требующий.сортировать.результаты. по.времени.\(time\).изменения:

Добавим.параметр.с.длинным.именем.--reverse,.чтобы.изменить.порядок.сорти-

ровки.на.обратный

```
root@8badb90a35b9:~# ls ~ /usr
/root:

/usr:
bin  games  include  lib  local  sbin  share  src

root@8badb90a35b9:~# ls /usr -l
total 32
drwxr-xr-x  2 root root 4096 May 26 00:45 bin
drwxr-xr-x  2 root root 4096 Apr 24 08:34 games
drwxr-xr-x  2 root root 4096 Apr 24 08:34 include
drwxr-xr-x 10 root root 4096 May 26 00:44 lib
drwxr-xr-x 10 root root 4096 May 26 00:44 local
drwxr-xr-x  1 root root 4096 Jun  5 21:20 sbin
drwxr-xr-x 33 root root 4096 May 26 00:44 share
drwxr-xr-x  2 root root 4096 Apr 24 08:34 src

root@8badb90a35b9:~# ls /usr -lt --reverse
total 32
drwxr-xr-x  2 root root 4096 Apr 24 08:34 src
drwxr-xr-x  2 root root 4096 Apr 24 08:34 include
drwxr-xr-x  2 root root 4096 Apr 24 08:34 games
drwxr-xr-x 10 root root 4096 May 26 00:44 local
drwxr-xr-x 33 root root 4096 May 26 00:44 share
drwxr-xr-x 10 root root 4096 May 26 00:44 lib
drwxr-xr-x  2 root root 4096 May 26 00:45 bin
drwxr-xr-x  1 root root 4096 Jun  5 21:20 sbin

root@8badb90a35b9:~# ls /usr              
bin  games  include  lib  local  sbin  share  src

root@8badb90a35b9:~# ls /usr -a
.  ..  bin  games  include  lib  local  sbin  share  src

root@8badb90a35b9:~# ls /usr -dl
drwxr-xr-x 1 root root 4096 May 26 00:44 /usr


```



