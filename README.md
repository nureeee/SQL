# 210513_과제

## 

sqlite> .open 'c:\\dd\\mydb'
sqlite> .mode column
sqlite> .header on
sqlite> create table movie(title, director, actor, audience)
   ...> ;
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
sqlite> .import 'c:\\dd\\m.txt' movie
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
sqlite> select * from movie;
title  director  actor  audience
-----  --------  -----  --------
해운대    윤제균       설경구    1139
광해     추창민       이병헌    1232
국제시장   윤재균       황정민    1318
도둑들    최동훈       전지현    1302
변호인    양우석       송강호    1137
sqlite> insert into movie values('명량', '김한민', '최민식', 1761);
sqlite> select * from movie;
title  director  actor  audience
-----  --------  -----  --------
해운대    윤제균       설경구    1139
광해     추창민       이병헌    1232
국제시장   윤재균       황정민    1318
도둑들    최동훈       전지현    1302
변호인    양우석       송강호    1137
명량     김한민       최민식    1761
sqlite> update movie set actor = '김혜수' where actor = '전지현';
sqlite> select * from movie;
title  director  actor  audience
-----  --------  -----  --------
해운대    윤제균       설경구    1139
광해     추창민       이병헌    1232
국제시장   윤재균       황정민    1318
도둑들    최동훈       김혜수    1302
변호인    양우석       송강호    1137
명량     김한민       최민식    1761
sqlite> delete form movie where title = '국제시장';
Error: near "form": syntax error
sqlite> delete from movie where title = '국제시장';
sqlite> select * from movie;
title  director  actor  audience
-----  --------  -----  --------
해운대    윤제균       설경구    1139
광해     추창민       이병헌    1232
도둑들    최동훈       김혜수    1302
변호인    양우석       송강호    1137
명량     김한민       최민식    1761
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
CREATE TABLE Man(name, age);
sqlite>
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
CREATE TABLE Man(name, age);
sqlite> select * from Man;
name  age
----  ---
김연아   32
손흥민   30
이강인   21
sqlite> .schema
CREATE TABLE movie(title, director, actor, audience);
CREATE TABLE Man(name, age);
sqlite> select * from movie;
title  director  actor  audience
-----  --------  -----  --------
해운대    윤제균       설경구    1139
광해     추창민       이병헌    1232
도둑들    최동훈       김혜수    1302
변호인    양우석       송강호    1137
명량     김한민       최민식    1761
sqlite> select * from movie order by audience desc;
title  director  actor  audience
-----  --------  -----  --------
도둑들    최동훈       김혜수    1302
광해     추창민       이병헌    1232
해운대    윤제균       설경구    1139
변호인    양우석       송강호    1137
명량     김한민       최민식    1761
