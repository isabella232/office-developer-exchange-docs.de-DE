---
title: Data (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: Das Data-Element enthält die Daten eines einzelnen exportierten Elements oder eines Elements, das in ein Postfach hochgeladen werden soll.
ms.openlocfilehash: 43ee16ca7caf634756ca00a88715d9834adad92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526970"
---
# <a name="data-base64binary"></a>Data (base64Binary)

Das **Data** -Element enthält die Daten eines einzelnen exportierten Elements oder eines Elements, das in ein Postfach hochgeladen werden soll. 
  
```XML
<Data/>
```

**xs: base64Binary**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung zum Exportieren eines einzelnen Post Fach Elements.  <br/> |
|[Element (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Das **Data** -Element enthält die Eigenschaftennamen und Werte für ein exportiertes Element oder ein Element, das in ein Postfach hochgeladen wird. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ExportItems-Vorgang](exportitems-operation.md)
- [UploadItems-Vorgang](uploaditems-operation.md)

