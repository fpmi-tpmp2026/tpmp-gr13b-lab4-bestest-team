# Documentation repository for lab 4
# "Fishing flotilla management system"

--- 
## Description
This is a repository for documenting the <a href="https://github.com/iliaamakarov/tpmp-lab4-code-publication">Fishing flotilla management system project</a> as well as for managing cooperative work through <a href="https://github.com/orgs/fpmi-tpmp2026/projects/16">projects</a>.

All documentation can be found on this repository's <a href="https://github.com/fpmi-tpmp2026/tpmp-gr13b-lab4-bestest-team/wiki">__wiki__</a>

This includes both the description for the main `flotilla` project as well as for the `personal` projects assigned seperately.

### Project description:<br>
This is a `C++` app for automating work with an `sqlite3` database through a command line interface.<br>
The program allows for automatic database creation (for testing purposes) and manual. The databases can be automatically cleaned up after testing is finishied.<br>
The app also includes functions described in the lab 4 assignment, such as `Selecting` entries based on different parameters and more specialized `functions` such as adding a bonus for catching more fish than planned.<br>

<details>
<summary>Task description</summary>
  Вариант 2. «Рыболовная флотилия».
Флотилия рыболовных траулеров осуществляет поиск косяков рыбы и его отлов. С этой
целью каждый траулер отправляется в рейс на некоторое количество суток и посещает ряд
мелководных участков моря, называемых банками. Каждая банка имеет свое название.
Выловленная рыба классифицируется своим названием, количеством и качеством.
Управление флотилией владеет информацией:
о траулерах: название траулера, водоизмещение, дата постройки;
о членах команды фамилия, должность, дата приема на работу, год рождения;
о результатах рейсов: название траулера, дата выхода в море, дата возращения, название
посещенной банки, название, качество и количество выловленной рыбы.
Член команды может узнать информацию: только свои данные - смотрите ниже по
пункту, помеченному * (звездочкой).
Необходимо выполнить:
1. Создать таблицы БД с учетом ограничений целостности данных.
2. Используя оператор Select, выдать следующую информацию:
 по указанному траулеру – перечень выполненных рейсов за указанный период с
выдачей сведений об общем количестве выловленной рыбы;
 по указанной банке – перечень и количество выловленной рыбы по видам рыбы;
 по банке, на которой было выловлено максимальное количество рыбы низкого
качества, – сведения о датах рейсов и траулерах, ее посещавших;
 по траулеру, выловившему наибольшее количество рыбы, – сведения о капитане и
посещенных траулером банках с указанием дат выхода и возвращения;
 по членам команд – перечень людей, которые на указанную дату должны быть
отправлены на пенсию.
3. Обеспечить с помощью операторов Insert, Update, Delete обновление информации в
указанных таблицах.
4. Создать функцию, который при добавлении информации в таблицу результатов рейса
выполняет обновление информации в таблице статистики, где для каждого траулера
хранится информация об общем количестве выловленной рыбы.
5. Создать функцию, которая за указанный период осуществляет начисление премий
членам экипажа за внеплановый отлов рыбы. В качестве параметра передать начальную
дату периода, конечную дату периода, плановое задание, среднюю стоимость килограмма
рыбы. Результаты занести в специальную таблицу(*).
6.Создать функцию, которая за указанный период осуществляет начисление премии
указанному члену экипажа(*)
</details>

<br>
The detailed description for the in-depth functionality of the project can be found on the <a href="https://github.com/iliaamakarov/tpmp-lab4-code-publication/blob/main/README.md">code publication repository</a>.

---

## Installation
clone the project's main repository:

`git clone https://github.com/iliaamakarov/tpmp-lab4-code-publication/blob/main/README.md`

run the make commands listed in the README.md (while in the cloned folder):

`make run` - run the application without creating a database

`make db` - create a seeded database from test data

`make clean` - clean compiled program and database files

`make test` - run built-in unit tests on the application, development purposes only

---

## Usage

### Viewing the database:
```
--- Welcome to Fishing Flotilla Management System ---
Username: captain
Password: password

Login successful. Welcome, captain (captain)

--- Captain Menu ---
1. Show trips by trawler
2. Show fish by bank
3. Show trips with max low-quality fish
4. Show captain of top trawler
5. Show retiring crew members
6. Add new crew member
7. Calculate bonus for unplanned catch
8. Calculate bonus for crew member
0. Logout
Enter choice: 1
```
### Specific trawler:
```
--- Trips for Trawler: Морской Волк from 2023-10-01 to 2023-11-30 ---
Trip ID              Exit Date            Return Date          Total Catch (kg)    
--------------------------------------------------------------------------------
1                    2023-10-01           2023-10-10           850                 
3                    2023-11-01           2023-11-10           1200
```
### Bonus for unplanned catch
```
Enter choice: 7

--- Calculating bonus for unplanned catch ---
Total unplanned catch: 350 kg.
Total bonus pool to distribute: 192.5
```
### Login
```
--- Welcome to Fishing Flotilla Management System ---
Username: crewman
Password: password

Login successful. Welcome, crewman (crewman)

--- Crewman Menu ---
1. View my data
0. Logout
Enter choice: 1

Displaying data for Петров
```
---

<br>

## Contributing

<a href="https://github.com/iliaamakarov">Ilia Makarov</a>

<a href="https://github.com/AbnerRoseline">Vadim Hursevich</a>
