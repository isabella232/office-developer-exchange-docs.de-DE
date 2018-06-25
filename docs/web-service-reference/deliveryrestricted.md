---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: Das DeliveryRestricted-Element gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.
ms.openlocfilehash: ba1c6e00b93c9e442a427fe98a5e15bf5fe1effd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757950"
---
# <a name="deliveryrestricted"></a>DeliveryRestricted

Das **DeliveryRestricted** -Element gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers. 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail-Infos](mailtips.md) <br/> |Stellt Werte für verschiedene Arten von e-Mail-Infos.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der dieses Element ist **true** , wenn die Zustellung Einschränkungen des Absenders der Nachricht verhindern Erreichen des Empfängers. Der Wert ist **false** , wenn Delivery Restrictions, nicht verhindert, dass der Nachricht des Absenders Erreichen des Empfängers. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

