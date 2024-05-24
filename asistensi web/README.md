MariaDB [(none)]> use tugasweb;
Database changed
MariaDB [tugasweb]> show tables;
+--------------------+
| Tables_in_tugasweb |
+--------------------+
| fakultas           |
| mahasiswa          |
| mahasiswa_fakultas |
+--------------------+
3 rows in set (0.007 sec)

MariaDB [tugasweb]> desc fakultas;
+---------------+--------------+------+-----+---------+----------------+
| Field         | Type         | Null | Key | Default | Extra          |
+---------------+--------------+------+-----+---------+----------------+
| id            | int(11)      | NO   | PRI | NULL    | auto_increment |
| nama_fakultas | varchar(100) | NO   |     | NULL    |                |
+---------------+--------------+------+-----+---------+----------------+
2 rows in set (0.037 sec)

MariaDB [tugasweb]> desc mahasiswa;
+--------+--------------+------+-----+---------+----------------+
| Field  | Type         | Null | Key | Default | Extra          |
+--------+--------------+------+-----+---------+----------------+
| id     | int(11)      | NO   | PRI | NULL    | auto_increment |
| nim    | varchar(15)  | NO   | UNI | NULL    |                |
| nama   | varchar(100) | NO   |     | NULL    |                |
| alamat | text         | NO   |     | NULL    |                |
+--------+--------------+------+-----+---------+----------------+
4 rows in set (0.022 sec)

MariaDB [tugasweb]> desc mahasiswa_fakultas;
+--------------+---------+------+-----+---------+----------------+
| Field        | Type    | Null | Key | Default | Extra          |
+--------------+---------+------+-----+---------+----------------+
| id           | int(11) | NO   | PRI | NULL    | auto_increment |
| mahasiswa_id | int(11) | NO   | MUL | NULL    |                |
| fakultas_id  | int(11) | NO   | MUL | NULL    |                |
+--------------+---------+------+-----+---------+----------------+
3 rows in set (0.025 sec)