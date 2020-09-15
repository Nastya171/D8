# D8
1) ���������� docker desktop [�����](https://www.docker.com/get-started) � ������ � ��������� `docker pull ubuntu` � `docker pull postgres`.
��� ������� ������ ����� ������� ��������� � ��������� ���, ��� ����� ����� ���� ������ ����� ������� `winpty docker run -it <image_name>` ���� ����� `docker container create --name my_container <image_name>` `winpty docker container start -it <name_container> bash`. ������� run - ����� ������� � ��������� ���������, �� ������ ������ ��� �������� ���������, --name - �������������� ����� ������� ������ ��� ����������, ����� ��� ����� ������ �������������, -it - ��� 2 ����� --interactive � --tty, ���� ����������� ����� ����� ������� ������ ������� ����������.

2) 
   - ������� Dockerfile, �� ����� � ����� docker � �������������.
   - ������� ����� �������� `docker build --tag my_image .` --tag/-t - ������ ��� ��� ������.
   - C������ ��������� �������� `docker container create --name my_container my_image`
   - ��������� ���������  `docker container start my_container`

3)
   - ```winpty docker exec -it my_container bash```
   - ```psql -h localhost -p 5432 -U postgres -W```
   - ```CREATE TABLE name_table (ID int primary key,Name text);```
   - ```insert into name_table values (1, 'Text');```
   - ```SELECT * FROM name_table;```
   - ```\q```
   - ```exit```
   - C������ ���� ```docker exec -t my_container pg_dumpall -c -U postgres > ./pg-init-scripts/dump_`date +%d-%m-%Y"_"%H_%M_%S`.sql```

4) Docker Compose ��������������� ������ � Docker desktop

5)
   - ������� �� ���������� ����
   - ������ `docker-compose -f docker-compose.yml up`
   - � �������� ����� �� http://localhost:8080/
   - ������� ������ PostgreSQL, ��� ������������ postgres, ������ example, ���� ������ postgres