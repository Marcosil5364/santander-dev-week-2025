# Santander dev-week-2023

JPA RESTful API criada pra dev week

classDiagram
    class Usuario {
        -String nome
        -Conta conta
        -Recurso[] recursos
        -Cartao cartao
        -Noticias[] noticias
    }

    class Conta {
        -String numero
        -String agencia
        -Numero saldo
        -Numero limite
    }

    class Feature {
        -String icone
        -String descricao
    }

    class Cartao {
        -String numero
        -Numero limite
    }

    class Noticias {
        -String icone
        -String descricao
    }

    Usuario "1" *-- "1" Conta
    Usuario "1" *-- "N" Recurso
    Usuario "1" *-- "1" Cartao
    Usuario "1" *-- "N" Noticias
