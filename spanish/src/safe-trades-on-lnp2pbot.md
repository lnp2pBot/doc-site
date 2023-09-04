# Intercambios seguros en @lnp2pbot

@lnp2pbot es una herramienta segura para el intercambio de bitcoin de forma p2p sin KYC debido a que cuando dos personas entran en contacto para hacer una compra-venta los Satoshis (Sats) del vendedor quedan retenidos en su propia wallet mediante una hold invoice y no los podrá utilizar mientras estén en dicho estado. Cuando el comprador de Sats envíe el dinero fíat, y el vendedor le confirme al bot que ya lo recibió, los Sats se enviarán hacia el nodo del bot y este los pagará al comprador lo antes posible.

El bot cuenta con un sistema de [reputación de los usuarios](https://lnp2pbot.com/aprende/how-does-the-user-reputation-system-work.html) que toma en cuenta la cantidad de operaciones exitosas y las calificaciones recibidas, además, muestra la cantidad de días que una persona ha estado utilizándolo. Estos datos pueden ayudarte a tomar decisiones sobre aceptar o rechazar ofertas según tus propios intereses.

Adicionalmente, cada comunidad del bot cuenta con al menos un Solver, quien es responsable de mediar en las disputas que puedan surgir, este solicitará las pruebas necesarias a las partes involucradas y determinará quién tiene razón y por tanto recibirá los Sats. Cuando se detecta a un estafador es baneado permanentemente y se le prohíbe seguir utilizando el bot.
