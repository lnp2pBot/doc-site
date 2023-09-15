# ¿Cómo funciona el sistema de reputación de usuario?

Por cada transacción que realices se te pedirá calificar a tu contraparte, a la vez que esta te calificará a ti. Para ello, [**lnp2pBot**](https://t.me/lnp2pBot) cuenta con un sistema de puntuación de 5 estrellas que te permitirá valorar tu experiencia, donde 1 estrella es la menor calificación y 5 estrellas es la mayor. 

Para obtener la reputación el bot realiza un cálculo iterativo de la media y la desviación estándar de las calificaciones y las operaciones exitosas, por lo que en las primeras operaciones, aunque te hayan calificado con el máximo, tu reputación no será alta sino que aumentará progresivamente a medida que vayas haciendo operaciones con buenas calificaciones. 

Dicho cálculo lo puedes ver en: [https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279](https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279)

Y está basado en:
[https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation](https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation)

Cuando crees una oferta, esta incluirá por defecto el número de operaciones exitosas que realizaste, las calificaciones recibidas de tus contrapartes, y el número de operaciones realizadas. Recomendamos tener en cuenta todos estos aspectos al tomar una oferta para evitar estafas.

![Reputation System](./assets/images/reputation-system.jpg)
