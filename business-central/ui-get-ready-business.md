---
title: Bienvenido | Documentos de Microsoft
description: "Describe las guías de configuración asistida, los vídeos, los temas de ayuda y las páginas y las ventanas que se usan para empezar a realizar operaciones empresariales en Business Central."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, setup, wizard, experience
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ddffef784a80227ea28b193779b4aead7c3b691a
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="getting-ready-for-doing-business"></a>Preparación para hacer negocios
Enhorabuena, acaba de iniciar su primera empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para ayudarle a empezar a hacer negocios, puede visitar la ventana **Asistencia de negocio** donde puede iniciar guías de configuración asistida, vídeos o temas de ayuda para determinadas tareas de configuración. A la ventana se accede desde el gráfico en el área de trabajo **Administrador de negocio** eligiendo el menú desplegable **Asistencia de negocio** y, a continuación, eligiendo la acción **Mostrar configuración y recursos de ayuda**. Al actualizar la página, el gráfico se reemplaza por los recursos de configuración y ayuda.

En el área de trabajo, en la barra de navegación superior, encontrará el menú **Configuración y extensiones**. Aquí tiene acceso a una lista de configuraciones asistidas que pueden ayudarle a empezar. Una vez haya migrado los datos, como los proveedores, clientes o productos de su sistema financiero existente, está listo para empezar. Pero en función de sus necesidades, considere si la otra configuración asistida puede ayudarle. Si un área no está cubierta por una configuración asistida, elija la acción **Configuración manual** para obtener acceso a las ventanas de configuración donde puede rellenar los campos de configuración de todas las áreas manualmente. Para obtener más información, consulte también [Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).

> [!NOTE]  
>   La lista de guías de configuración, las extensiones y los servicios que están disponibles varían según la experiencia del usuario que elija para la empresa. La experiencia **Esencial** ofrece menos acceso que la experiencia **Premium**. La primera vez que inicie sesión, use la experiencia Esencial. Para obtener más información, consulte [Cambiar las funciones que se muestran](ui-experiences.md).

En la ventana **Configuración asistida**, encontrará lo siguiente con la experiencia **Esencial**:

| Configuración asistida | Description |
| --- | --- |
| Configurar la empresa |Crea una nueva empresa de prueba para que pueda introducir datos y probar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si empezó con el paseo de introducción, es probable que ya lo haya **Completado**. |
| Migrar datos empresariales |Permite importar datos empresariales existentes, como proveedores, clientes y productos desde Excel o Quickbooks. |
| Configurar impuestos de ventas |Le ayudará a empezar con grupos de impuestos por defecto y asignará códigos de impuestos de área que podrá asignar a clientes y proveedores para poder calcular automáticamente los impuestos de venta en los documentos de venta o compra. |
| Configurar correo electrónico |Le prepara para enviar correos electrónicos directamente de, por ejemplo, pedidos o contactos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
| Configurar complementos de Office |Le posibilita usar y ejecutar [!INCLUDE[d365fin](includes/d365fin_md.md)] desde Outlook. |
| Config. flujo trabajo aprob. |Le permite notificar automáticamente al aprobador cuando un usuario intente crear o cambiar determinados valores en documentos, líneas de diario o tarjetas, como por ejemplo un importe por encima del límite especificado. |
| Config. registro correo elect. |Le permite iniciar sesión en la correspondencia por correo electrónico en [!INCLUDE[d365fin](includes/d365fin_md.md)] para realizar el seguimiento de las interacciones. |
| Configurar el conector de Business Central |Le permite conectar con Dynamics 365 for Sales que le posibilita la sincronización de datos como los contactos y la información de los pedidos. |

Cuando ha ejecutado un asistente de configuración, se marca como **Completado**. Para ejecutar el asistente de configuración, seleccione los tres puntos también denominados menú contextual y, a continuación, seleccione **Iniciar configuración**.

## <a name="role-center"></a>Área de trabajo
En Área de trabajo tiene información general de su negocio. A la izquierda puede ver una barra de navegación que le da un acceso sencillo a los clientes, proveedores, productos, etc. En el centro se encuentra el mosaico **Actividades**. **Actividades** muestra los datos actuales y se puede hacer clic o pinchar sobre él para conseguir un acceso fácil al documento seleccionado. Los **Indicadores de rendimiento clave** pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos. También puede crear una lista de **Clientes favoritos** en el área de trabajo para las cuentas con las que hace negocios a menudo o a las que necesita prestar especial atención.
Use las flechas para contraer parte de la página y haga más espacio para mostrar datos específicos. En la parte superior del área de trabajo encontrará todas las acciones que se pueden realizar con el contenido actual. Todo esto también se puede contraer y solo necesita hacer clic o pinchar en el área contraída para volverlo a ver.

> [!TIP]  
> Puede volver al área de trabajo seleccionando el nombre de la empresa en la esquina superior izquierda.

## <a name="company-information"></a>Información de empresa
En **Configuración de la empresa** puede ver y editar información de configuración sobre la empresa actual, mucha de la cual se rellenó previamente si completó la configuración asistida **Configurar empresa** al registrarse en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si desea cambiar el logotipo de la empresa, la información de contacto, la configuración del banco o la información de los impuestos, puede hacerlo desde esta ventana.    

## <a name="adding-users-and-permissions"></a>Agregar usuarios y permisos
Si necesita agregar más usuarios, se realiza de centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc). Una vez se hayan creado los usuarios en Office 365, se pueden importar en la ventana **Usuarios** mediante la acción **Obtener usuarios desde Office 365**. Después podrá continuar con la asignación de permisos a usuarios y la organización en grupos de usuarios. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).  

## <a name="getting-help"></a>Obtener ayuda
En [!INCLUDE[d365fin](includes/d365fin_md.md)] encontrará las herramientas de información que pueden guiarle a través de varios procesos empresariales. En cada herramienta de información encontrará un vínculo denominado **Obtener ayuda** que le llevará a la ayuda del producto. El signo de interrogación de la esquina superior derecha también le dirige a la ayuda del producto.

## <a name="next-steps"></a>Pasos siguientes
Según sus datos migrados, ahora puede empezar a crear nuevos documentos de compra o venta. Use la sección **Mi empresa** de la ventana **Inicio** para crear rápidamente una nueva oferta de venta, factura de venta, pedido de venta, factura de compra o registro de venta.

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

