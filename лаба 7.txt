CREATE TABLE myfamily (
    id integer PRIMARY KEY,
    name varchar,
    gender varchar,
    age integer,
    role integer,
    hobbie integer
);
CREATE TABLE hobbie (
    id integer PRIMARY KEY,
    description varchar
);
CREATE TABLE role (
    id integer PRIMARY KEY,
    description varchar
);


INSERT INTO myfamily values (1,'Artem', 'male', 19, 5, 1);
INSERT INTO myfamily values (2,'Olga', 'female', 44, 2, 5);
INSERT INTO myfamily values (3,'Vadim', 'male', 11, 4, 3);
INSERT INTO myfamily values (4,'Gennadiy', 'male', 45, 1, 6);
INSERT INTO myfamily values (5,'Diana', 'female', 19, 3, 2);
INSERT INTO myfamily values (6,'Evgeniy', 'male', 41, 1, 6);
INSERT INTO myfamily values (7,'DmitriyMaslennikov', 'male', 9, 4, 7);
INSERT INTO myfamily values (8,'EkaterinaVtoraye', 'female', 40, 2, 8);

INSERT INTO hobbie values (1, 'Sport');
INSERT INTO hobbie values (2, 'Dance');
INSERT INTO hobbie values (3, 'Football');
INSERT INTO hobbie values (4, 'Voleyball');
INSERT INTO hobbie values (5, 'Sing');
INSERT INTO hobbie values (6, 'Ride');
INSERT INTO hobbie values (7, 'Games');
INSERT INTO hobbie values (8, 'Read');

INSERT INTO role values (1, 'Dad');
INSERT INTO role values (2, 'Mother');
INSERT INTO role values (3, 'Doughter');
INSERT INTO role values (4, 'YongerSon');
INSERT INTO role values (5, 'Son');

UPDATE myfamily SET hobbie = 7 WHERE id = 3;
DELETE FROM myfamily WHERE id = 1;
SELECT myfamily.id, name, gender, age, role.description, hobbie.description FROM myfamily 
LEFT JOIN role ON myfamily.role=role.id
LEFT JOIN hobbie ON myfamily.hobbie=hobbie.id
WHERE gender = 'male'

ORDER BY myfamily.age DESC;