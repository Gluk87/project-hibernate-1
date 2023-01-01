# Проект Hibernate#1
БД Postgres. Запуск через Docker:
![alt text](https://github.com/Gluk87/project-hibernate-1/blob/dev/img/docker_db.png)

Генерация id решена через sequence:

create sequence rpg.player_seq
minvalue 41
owned by rpg.player.id;

@GeneratedValue(strategy = GenerationType.SEQUENCE, generator = "player_seq")
@SequenceGenerator(name="player_seq", sequenceName="rpg.player_seq", allocationSize=1)

![alt text](https://github.com/Gluk87/project-hibernate-1/blob/dev/img/create.png)

Работа p6spy:
![alt text](https://github.com/Gluk87/project-hibernate-1/blob/dev/img/p6spy.png)