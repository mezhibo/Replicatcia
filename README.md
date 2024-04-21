Задание 1.

На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.

Решение 1.

Master-slave репликация представляет собой асимметричную структуру, где один сервер базы данных (master) является источником данных, а другие серверы базы данных (slaves) получают копии данных и обновляют их в соответствии с изменениями, произошедшими на master. Таким образом, все операции записи (INSERT, UPDATE, DELETE) выполняются только на master-сервере, и данные синхронизируются с slave-серверами.

Master-master репликация также известна как симметричная или взаимная репликация. При такой конфигурации каждый сервер базы данных может быть использован как master и slave одновременно. Это означает, что каждый узел может принимать операции записи и изменения данных, которые затем реплицируются на другие узлы. Это обеспечивает более высокую отказоустойчивость и распределенную нагрузку.

Сравним master-slave и master-master репликацию по нескольким параметрам:

1. Пропускная способность: master-slave репликация имеет ограниченную пропускную способность из-за необходимости записывать все данные на master-сервере, в то время как master-master репликация может распределять нагрузку на запись между узлами, что повышает пропускную способность и увеличивает масштабируемость.

2. Доступность: master-slave репликация обеспечивает более простую реализацию и поддержку, тогда как master-master репликация требует более сложной настройки и обработки конфликтов при возникновении. Однако, master-master репликация обеспечивает более высокую доступность из-за возможности использования любого узла для чтения и записи.

3. Стабильность и консистентность данных: в master-master репликации существует риск конфликтов данных при одновременных записях на разных узлах, что требует дополнительных мер для обеспечения консистентности. В то время как в master-slave репликации данные всегда консистентны, поскольку записи происходят только на master-сервере.

4. Распределение нагрузки: master-master репликация позволяет лучше распределить нагрузку между узлами, что улучшает производительность и масштабируемость. В то время как в master-slave репликации все операции записи должны быть выполнены на одном узле, что может привести к узким местам и перегрузке.

Выбор между master-slave и master-master репликацией зависит от требований к системе, масштабируемости, доступности данных и других факторов. Некоторые системы могут воспользоваться комбинацией обеих форм репликации для обеспечения наилучшей производительности и отказоустойчивости.



Задание 2

Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

Приложите скриншоты конфигурации, выполнения работы: состояния и режимы работы серверов.


Решение 2.

![alt text](https://github.com/mezhibo/Replicatcia/blob/34490b0dc1df2179347a4ced8e086db61fbd04de/IMG/2.jpg)


![alt text](https://github.com/mezhibo/Replicatcia/blob/34490b0dc1df2179347a4ced8e086db61fbd04de/IMG/3.jpg)


![alt text](https://github.com/mezhibo/Replicatcia/blob/34490b0dc1df2179347a4ced8e086db61fbd04de/IMG/4.jpg)

