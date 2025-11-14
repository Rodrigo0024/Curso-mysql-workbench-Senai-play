-- subconsulta no select

select Nome, (select count(\*) from pedidos where clienteID = c.ClienteID) as Numeropedidos
from clientes c;

-- Subconsultas utilizadas na clausula FROM
select a.Saldo
from( select ClienteID,sum(valor) as Saldo from pedidos Group by ClienteID) a

limit 0,1000;

-- subconsultas no WHERE
select Nome, Email
from clientes
where ClienteID in(select ClienteID from pedidos where Valor >50);

-- Consulta complexa
SELECT
c.Nome,
p.Produto,
p.Quantidade
FROM Clientes c
JOIN Pedidos p
ON c.ClienteID = p.ClienteID
WHERE
p.Quantidade > (

    SELECT
      AVG(Quantidade)
    FROM Pedidos

);
