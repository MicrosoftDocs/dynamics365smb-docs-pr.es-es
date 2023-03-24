---
author: edupont04
ms.topic: include
ms.date: 05/09/2022
ms.author: edupont
---
Es posible que vea a otros usuarios en la lista **Usuarios** aparte de los de su propia empresa. Cuando un administrador delegado de una empresa asociada distribuidora inicia sesión en un entorno de [!INCLUDE [prod_short](prod_short.md)] en nombre de su cliente, se crea automáticamente como un usuario dentro [!INCLUDE [prod_short](prod_short.md)]. De esta forma, las acciones realizadas por un administrador delegado quedan registradas en [!INCLUDE [prod_short](prod_short.md)], como la publicación de documentos, y asociados con su id. de usuario.  

Con *Privilegios de administrador delegados granulares (GDAP)*, el usuario se muestra en la lista **Usuarios** y se le puede asignar cualquier permiso. No se muestran con el nombre y otra información personal, sino con el nombre de su empresa y una identificación única. Tanto los administradores internos como los externos pueden ver a estos usuarios en la lista **Usuarios** y tienen total transparencia en lo que estos usuarios hacen a través del [registro de cambios](../across-log-changes.md), por ejemplo. Pero no pueden ver el nombre real de estos usuarios. Los usuarios de GDAP se enumeran con nombres de usuario en el siguiente formato: `User123456@partnerdomain.com`. Es posible que tengan un nombre de usuario que refleje el nombre de la empresa del socio y la dirección de correo electrónico no sea la dirección de correo electrónico real de la persona. De esta forma, las cuentas de usuario del GDAP no revelan información personal. Si necesita averiguar quién es la persona detrás de dicho seudónimo, deberá comunicarse con la empresa para la que trabaja o trabajaba este usuario.  
