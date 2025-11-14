CREATE TABLE `empresa`.`pedidos` (
`idPedidos` INT NOT NULL AUTO_INCREMENT,
`ClienteID` INT NULL,
`DataPedido` DATE NULL,
PRIMARY KEY (`idPedidos`));

alter table `empresa`. `pedidos`
ADD index `fk_cliente_idx`(`ClienteID`);

ALTER TABLE `empresa`.`pedidos`
ADD CONSTRAINT `fk_clienteID`
FOREIGN KEY (`ClienteID`)
REFERENCES `empresa`.`cliente` (`idCliente`)
ON DELETE CASCADE
ON UPDATE CASCADE;
