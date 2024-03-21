---
title: Configurar comprobantes digitales
description: Este artículo explica cómo configurar y utilizar vales digitales obligatorios en Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# Configurar comprobantes digitales

Los administradores pueden utilizar la funcionalidad de comprobante digital para exigir que los documentos se adjunten a transacciones específicas cuando se publiquen. Por lo tanto, esta funcionalidad permite un enfoque basado en el origen y proporciona un mejor seguimiento de auditoría. Para ello se pueden configurar diferentes tipos de cumplimiento, dependiendo de los documentos o tipos de diario.

El término *bono digital* se refiere a una forma digital o electrónica de un comprobante tradicional en contabilidad. Un comprobante es un documento que se utiliza para respaldar y autorizar transacciones financieras. En contabilidad, un comprobante suele servir como prueba de un gasto o de un recibo de fondos. El comprobante puede incluir detalles como la fecha de la transacción, una descripción, el monto y cualquier firma de autorización.

> [!IMPORTANT]
> En algunos países y regiones, es posible que no pueda configurar algunas opciones, ya que es posible que los requisitos legales exijan configuraciones específicas. Si encuentra estas restricciones, busque una explicación detallada en la página de documentación de su país o región.

## Habilitar comprobantes digitales

Siga estos pasos para habilitar la funcionalidad de vale digital.

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de vale digital** y luego seleccione el vínculo relacionado.
2. Seleccione la casilla de verificación **Habilitado**.

## Configurar comprobantes digitales

Puede utilizar diferentes configuraciones para los siguientes documentos y diarios.

| Tipo movimiento | Descripción |
|------------|-------------|
| Documento de venta | Especifica contabilizaciones que se completan a partir de documentos de ventas. |
| Documento compra | Especifica contabilizaciones que se completan a partir de documentos de compra. |
| Diario general | Especifica las contabilizaciones que se completan desde el diario general para todos los tipos de cuentas excepto aquellas relacionadas con el cliente y el proveedor. Si selecciona uno de esos tipos de cuenta, cambia el control del proceso de publicación. Si selecciona **Cliente** como tipo de cuenta, el sistema verifica su configuración relacionada con el diario de ventas. Si selecciona **Proveedor** como tipo de cuenta, el sistema verifica su configuración relacionada con el diario de compras. |
| Diario ventas | Especifica las contabilizaciones que se completan desde el diario de ventas y el diario general donde **Cliente** está seleccionado como tipo de cuenta. |
| Diario compras | Especifica las contabilizaciones que se completan desde el diario de compras y el diario general donde **Proveedor** está seleccionado como tipo de cuenta. |

Siga estos pasos para definir cómo su organización utiliza los vales digitales obligatorios.

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de entrada de vale digital** y luego seleccione el vínculo relacionado. Alternativamente, en la página **Configuración de vales digitales**, seleccione **Configuración de entrada**.
2. En la columna **Tipo de entrada**, seleccione una opción.
3. En la columna **Tipo de comprobación**, seleccione una opción obligatoria. Si selecciona **Ninguno**, puede publicar el tipo de entrada seleccionado sin un comprobante digital. Si selecciona **Adjunto**, la entrada debe incluir un archivo adjunto. Si selecciona **Anexo o nota**, puede incluir un archivo adjunto o una nota para la entrada. 
4. Seleccione la casilla **Generar automáticamente** para generar el comprobante digital automáticamente. Por ejemplo, si no desea agregar manualmente una factura de venta a su transacción, seleccione esta casilla de verificación. Luego, sólo tienes que publicar el documento. El sistema crea automáticamente el documento, según el diseño de su informe, y lo adjunta a la transacción.
5. Seleccione la casilla **Omitir si se agrega manualmente** si no desea agregar un cupón digital generado automáticamente si el usuario ya agregó un archivo adjunto manual.

### Utilice códigos fuente para la configuración

Para utilizar el cumplimiento para los diarios, pero no para todos los tipos de transacciones, conecte el código fuente específico para identificar el tipo de entrada: diario general, diario de ventas o diario de compras.

Siga estos pasos para configurar códigos fuente específicos para vales digitales.

1. Sobre la página **Configuración de entrada de vales digitales**, seleccione **Códigos fuente**.
2. Sobre la página **Códigos fuente de entrada de vales**, seleccione los códigos fuente que desea configurar.
3. Cierre la página.

## Usar la funcionalidad

Abra un documento de compra o venta e ingrese información en los campos obligatorios. Antes de publicar el documento, debes seguir estos pasos para adjuntar un comprobante digital.

1. En el cuadro informativo **Archivos de documentos entrantes**, seleccione **Adjuntar archivo**.
2. Arrastre un archivo directamente a la página **Insertar archivo** o busque el archivo desde esta página.

El documento se adjunta al cuadro informativo **Archivos de documentos entrantes**. Para cada línea, puede encontrar el nombre y el tipo del documento.

Si accidentalmente adjunta el comprobante incorrecto, siga estos pasos para eliminarlo antes de publicar el documento.

1. En el cuadro informativo **Archivos de documentos entrantes** de la línea del documento, seleccione **Documento entrante**.
2. Sobre la página **Documento entrante**, seleccione **Eliminar**.

> [!NOTE]
> Si el adjunto de un comprobante digital está configurado como obligatorio e intenta publicar documentos o diarios sin adjuntar un comprobante, el sistema le impide publicar. Recibe el siguiente mensaje de error: "No es posible publicar sin adjuntar el comprobante digital".

### Buscar comprobantes adjuntos en transacciones

Puede encontrar el comprobante adjunto en el documento publicado o en la página **Movimientos del libro mayor** buscando en el cuadro informativo **Archivos de documentos entrantes**.

No puede eliminar un documento adjunto una vez completada la publicación. Sin embargo, puede agregar más archivos adjuntos una vez completada la publicación.

## Consulte también .

[Gestión financiera](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
