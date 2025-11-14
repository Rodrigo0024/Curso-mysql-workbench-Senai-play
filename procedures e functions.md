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

DELIMITER //

CREATE FUNCTION calcularIVA (
valor DECIMAL(10, 2)
)
RETURNS DECIMAL (10, 2)
DETERMINISTIC
BEGIN
--
RETURN valor \* 0.15;
END //

DELIMITER ;
