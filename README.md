docker run -d --name kudu-impala -p 21000:21000 -p 21050:21050 -p 25000:25000 -p 25010:25010 -p 25020:25020 apache/kudu:impala-latest impala<br>
docker exec -it kudu-impala impala-shell<br>
CREATE DATABASE my_database;

USE my_database;

CREATE TABLE users ( id INT,
    name text,
    age INT );

INSERT INTO users VALUES
    (1, 'Alice', 30),
    (2, 'Bob', 35),
    (3, 'Charlie', 25);

SELECT * FROM users;
<br>
docker stop kudu-impala
     docker rm kudu-impala
<br>

object Hello {
    def main(args: Array[String]) = {
        println("Hello, world")
    }
}
