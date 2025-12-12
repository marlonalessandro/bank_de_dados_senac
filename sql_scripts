CREATE DATABASE IF NOT EXISTS pizzaria_bella;
USE pizzaria_bella;
CREATE TABLE IF NOT EXISTS clientes (
  cliente_id INT NOT NULL AUTO_INCREMENT,
  nome VARCHAR(100) NOT NULL,
  telefone VARCHAR(20),
  cidade VARCHAR(50),
  PRIMARY KEY (cliente_id)
) ENGINE = InnoDB;

CREATE TABLE IF NOT EXISTS pizzas (
  pizza_id INT NOT NULL AUTO_INCREMENT,
  nome_pizza VARCHAR(100) NOT NULL,
  categoria VARCHAR(50) NOT NULL,
  preco DECIMAL(8,2) NOT NULL,
  PRIMARY KEY (pizza_id)
) ENGINE = InnoDB;

CREATE TABLE IF NOT EXISTS pedidos (
  pedido_id INT NOT NULL AUTO_INCREMENT,
  cliente_id INT NOT NULL,
  pizza_id INT NOT NULL,
  data_pedido DATE NOT NULL,
  quantidade INT NOT NULL,
  valor_total DECIMAL(8,2) NOT NULL,
  PRIMARY KEY (pedido_id),
  INDEX fk_cliente_id_idx (cliente_id),
  INDEX fk_pizza_pedidos_idx (pizza_id),
  CONSTRAINT fk_cliente_pedidos
    FOREIGN KEY (cliente_id)
    REFERENCES clientes (cliente_id)
    ON DELETE RESTRICT
    ON UPDATE NO ACTION,
  CONSTRAINT fk_pizza_pedidos
    FOREIGN KEY (pizza_id)
    REFERENCES pizzas (pizza_id)
    ON DELETE RESTRICT
    ON UPDATE NO ACTION
) ENGINE = InnoDB;
