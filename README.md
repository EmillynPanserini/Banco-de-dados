# SQL

integer
real
serial
numeric

varchar(n)
char(n)
text

boolean

date
time
timestamp

CREATE TABLE aluno(
    id SERIAL,
	nome VARCHAR(255),
	cpf CHAR (11),
	observacao TEXT,
	idade INTEGER,
	dinheiro NUMERIC (10,2),
	altura real,
	ativo BOOLEAN,
	data_nascimento DATE,
	hora_aula TIME,
	matriculado_em timestamp
);

SELECT *
FROM aluno;

INSERT INTO aluno(
	nome, 
	cpf,
	observacao,
	idade,
	dinheiro,
	altura,
	ativo,
	data_nascimento,
	hora_aula,
	matriculado_em
)
VALUES(
	'Emillyn',
	'65224796320',
	'aluno ads',
	20,
	600.20,
	1.60,
	TRUE,
	'2003/08/04',
	'17:50:00',
	'2024-02-21 10:09:00'
	
);

SELECT *
	FROM aluno
WHERE id =1;

UPDATE aluno 
	SET nome = 'Yuumi', 
	cpf= '13225369870',
	observacao = 'curso adm',
	idade = 21,
	dinheiro = '200.20',
	altura = '2.00',
	ativo = FALSE,
	data_nascimento = '25-02-2022',
	hora_aula = '15:00:00',
	matriculado_em = '2024-02-01 17:00:00'
WHERE id = 1;

SELECT *
	FROM aluno
	WHERE nome ='Yuumi';

DELETE 
	FROM aluno
WHERE nome = 'Yuumi';
