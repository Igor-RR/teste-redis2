Exercicios:

1)  127.0.0.1:6379> SET usuario "Carlos"
    OK
    127.0.0.1:6379> GET usuario
    "Carlos"
    127.0.0.1:6379> SET usuario "Carlos Silva"
    OK

2)
    127.0.0.1:6379> MSET produto "Notebook" preco "3500" estoque "15"
    OK
    127.0.0.1:6379> MGET produto preco estoque
    1) "Notebook"
    2) "3500"
    3) "15"

3)  
    127.0.0.1:6379> SETNX admin me
    (integer) 1
    127.0.0.1:6379> SETNX admin other
    (integer) 0
    127.0.0.1:6379> GET admin
    "me"
    127.0.0.1:6379> 

4)  127.0.0.1:6379> SET nome "Maria"
    OK
    127.0.0.1:6379>  SET nome "Maria Oliveira"
    OK
    127.0.0.1:6379> STRLEN nome
    (integer) 14
    127.0.0.1:6379> GETRANGE nome 0 5
    "Maria "

5)  127.0.0.1:6379> SET cidade "Campinas" 
    OK
    127.0.0.1:6379> SETRANGE cidade 0 "São "
    (integer) 8
    127.0.0.1:6379> GET cidade
    "S\xc3\xa3o nas"
1   27.0.0.1:6379> 

    --------- /* Para a correção do texto */ ------------
    (main) $ docker compose exec redis redis-cli --raw
    127.0.0.1:6379> GET cidade
    Campinas
    127.0.0.1:6379> SETRANGE cidade 0 "São "
    8
    127.0.0.1:6379> GET cidade
    São nas

6)  127.0.0.1:6379> SET pontos 10
    OK
    127.0.0.1:6379> INCRBY pontos 1
    11
    127.0.0.1:6379> INCRBY pontos 5
    16
    127.0.0.1:6379> DECRBY pontos 3
    13
    127.0.0.1:6379> GET pontos
    13

7)  127.0.0.1:6379> SET saldo 100.500
    OK
    127.0.0.1:6379> INCRBYFLOAT saldo 25.75
    126.25
    127.0.0.1:6379> GET saldo
    126.25

8)  SET token "AH22"
    127.0.0.1:6379> EXPIRE token 60
    1
    127.0.0.1:6379> TTL token
    53


    
