# Creando órdenes

El funcionamiento del bot sigue siendo exactamente igual, por defecto crea las órdenes en un canal global. Pero como hemos creado una nueva comunidad queremos que nuestra orden sea publicada en el canal que hemos asociado a la comunidad. Hay dos maneras de crear una orden en la nueva comunidad.

Entramos al grupo de la comunidad (en el caso de nuestro ejemplo sería @p2pZimbabwe) y dentro del grupo ejecutamos el comando de siempre: `/sell` o `/buy`.
Si queremos algo más privado, le indicamos al bot nuestra comunidad por defecto ejecutando el comando `/setcomm @p2pZimbabwe`. A partir de ese momento, todas las órdenes que crees en privado irán al canal correspondiente vinculado con @p2pZimbabwe. Puedes cambiar tu comunidad por defecto cuando quieras con `/setcomm @ComunidadMuchoMasCool` (ejemplo). También puedes volver al estado anterior, donde no tenías una comunidad por defecto, ejecutando `/setcomm off`.
