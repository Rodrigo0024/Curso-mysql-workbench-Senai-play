select c.nome, v.marca,v.modelo
from clientes c inner join veiculos v on c.idCliente = v.idCliente;

-- Lista clientes, modelo e marca se houver, se não colocar o null

select c.nome, v.marca,v.modelo
from clientes c left join veiculos v on c.idCliente = v.idCliente;

select c.nome, v.marca,v.modelo
from clientes c right join veiculos v on c.idCliente = v.idCliente;
