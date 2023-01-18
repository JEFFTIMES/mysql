# Allow remote access

[reference](https://stackoverflow.com/questions/1559955/host-xxx-xx-xxx-xxx-is-not-allowed-to-connect-to-this-mysql-server)

- SQL code

      mysql> CREATE USER 'monty'@'localhost' IDENTIFIED BY  'some_pass';
      mysql> GRANT ALL PRIVILEGES ON *.* TO 'monty'@'localhost'
          ->     WITH GRANT OPTION;
      mysql> CREATE USER 'monty'@'%' IDENTIFIED BY 'some_pass';
      mysql> GRANT ALL PRIVILEGES ON *.* TO 'monty'@'%'
          ->     WITH GRANT OPTION;
