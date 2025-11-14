DELIMITER //

CREATE PROCEDURE inserir_cliente (
IN p_nome VARCHAR(255),
IN p_email VARCHAR(255)
)
BEGIN
INSERT INTO Clientes (nome, email) VALUES (p_nome, p_email);
END //

DELIMITER ;

call inserir_cliente('Pamela Silva Barros', 'Pamela@gmail.com');
select \* from clientes;
