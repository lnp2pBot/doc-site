# ¿Qué tasa de cambio utiliza el bot?

Al crear una orden puedes optar por especificar solo el monto fíat a `pagar/cobrar`, y no la cantidad de sats que deseas `comprar/vender`. En este caso, debes seleccionar el botón `Precio de mercado`, y el bot hará el cálculo a tasa de mercado ofrecida por [yadio.io](https://yadio.io/) en el momento en que tu orden sea tomada.

![Precio de mercado](./assets/images/market-price.gif)

Cuando seleccionas el botón `Precio de mercado` también puedes colocar una prima o un descuento para tu oferta, esto significa que se aplicará un aumento o una disminución al precio de bitcoin que marque [yadio.io](https://yadio.io/) en el momento en que se tome.

#### Ejemplos prácticos con su significado:

- Compro Sats  +1%: Quiero comprar Sats un 1% más caro (por encima) que el precio de BTC que marque [yadio.io](https://yadio.io/) al momento en que alguien tome mi oferta. 

- Compro Sats -5%: Quiero comprar Sats un 5% más barato (por debajo) que el precio de BTC que marque [yadio.io](https://yadio.io/) al momento en que alguien tome mi oferta.

- Vendo Sats +3%: Quiero vender Sats un 3% más caro (por encima) que el precio de BTC que marque [yadio.io](https://yadio.io/) al momento en que alguien tome mi oferta.

- Vendo Sats -4%: Quiero vender Sats un 4% más barato (por debajo) que el precio de BTC que marque [yadio.io](https://yadio.io/) al momento en que alguien tome mi oferta.
