# MaratonaDev3.0
Desenvolvimento de site para cadastro de lista de doadores de sangue na semana MaratonaDev 3.0 da RocketSeat. Tecnologias utilizadas: Javascript, CSS, HTML e SQL Postgres

![image](https://user-images.githubusercontent.com/40874927/75614006-a8ef1080-5b12-11ea-872f-bcc927be70f9.png)

![image](https://user-images.githubusercontent.com/40874927/75614028-d50a9180-5b12-11ea-9f8b-9deda368421b.png)

Para rodar a aplicação é necessário ter o Postgres configurado.

1 → Criar tabela donors: 
-- Table: public.donors

-- DROP TABLE public.donors;

CREATE TABLE public.donors
(
    id integer NOT NULL DEFAULT nextval('donors_id_seq'::regclass),
    name text COLLATE pg_catalog."default" NOT NULL,
    email text COLLATE pg_catalog."default" NOT NULL,
    blood text COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT pk_id_donors PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE public.donors
    OWNER to postgres;

2 → No arquivo server.js pode ser necessário alterar as informações de conexão com banco de dados, localizadas na constante "db"

3 → No terminal deve-se executar o comando npm start, a mensagem "iniciei o servidor" aparecerá, caso não haja erros.
    
