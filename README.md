## 10-monitoring-02-systems

**Опишите основные плюсы и минусы pull и push систем мониторинга.**  
push:  
Все централизовано, поэтому очень легко вносить глобальные и широкие или узкие изменения.
мы можем добавлять или изменять метрики мониторинга или частоты и т.д. для отдельных групп хостов, которые имеют проблемы. Новая информация поступает почти мгновенно.
Центральные системы часто имеют шаблоны, что позволяет очень быстро и легко определять новые хосты и службы, наследуя все необходимое от существующих шаблонов. Это позволяет за считанные секунды установить комплекс мониторинга нового хоста

Pull:  
Pull (конфигурационные элементы, определяемые агентом) также великолепны, поскольку централизованное управление, направляющее конфигурационные элементы агентам, не является ни безупречным, ни идеальным решением:
Pull-системы обычно принимают специальные и незапланированные метрики в любое время или даже «одинаковую» метрику с различными единицами измерения, тэгами и т.д. Это большое преимущество Pull, особенно в мире DevOps, когда разработчики могут решить в любое время добавить метрики
Pull, как правило, являются более «современными» и лучше принимают тэги и дополнительные метаданные с метриками. 


**Какие из ниже перечисленных систем относятся к push модели, а какие к pull? А может есть гибридные?**

Prometheus - pull  
TICK - pull  
Zabbix - hybrid (usually pushing)  
VictoriaMetrics - hybrid  
Nagios - hybrid (usually pushing)  

**В виде решения на это упражнение приведите выводы команд с вашего компьютера (виртуальной машины):**
root@ubuntu:/home/sergey/netology/sandbox# curl http://localhost:8086
404 page not found
root@ubuntu:/home/sergey/netology/sandbox# curl http://localhost:8086/ping
root@ubuntu:/home/sergey/netology/sandbox# curl http://localhost:8888
<!DOCTYPE html><html><head><meta http-equiv="Content-type" content="text/html; charset=utf-8"><title>Chronograf</title><link rel="icon shortcut" href="/favicon.fa749080.ico"><link rel="stylesheet" href="/src.d80ed715.css"></head><body> <div id="react-root" data-basepath=""></div> <script src="/src.c278d833.js"></script> </body></html>root@ubuntu:/home/sergey/netology/sandbox# 
root@ubuntu:/home/sergey/netology/sandbox# curl http://localhost:9092/kapacitor/v1/ping
root@ubuntu:/home/sergey/netology/sandbox# curl http://localhost:3010
<!doctype html>
<html>
![image](https://user-images.githubusercontent.com/67621467/134769693-ae5f0ee1-8b57-4527-978a-086901fcf1ba.png)

*я не нашел кнопок и полей из ДЗ, возможно что-то успели изменить. в целом интерфейс выглядит так:*
  ![image](https://user-images.githubusercontent.com/67621467/134770023-0b394a30-4aa0-4873-befd-479cd74418e6.png)

  
