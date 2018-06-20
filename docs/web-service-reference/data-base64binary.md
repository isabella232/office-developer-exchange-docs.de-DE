---
title: Daten (base64Binary)
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
description: Data-Element enthält die Daten von einem einzelnen exportierten Element oder ein Element in einem Postfach hochladen.
ms.openlocfilehash: 9560273e31a64edb2254489961733dfe7360ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757844"
---
# <a name="data-base64binary"></a>Daten (base64Binary)

**Data** -Element enthält die Daten von einem einzelnen exportierten Element oder ein Element in einem Postfach hochladen. 
  
```XML
<Data/>
```

**xs:base64Binary**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach-Element zu exportieren.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element in einem Postfach hochladen.  <br/> |
   
## <a name="text-value"></a>Textwert

**Data** -Element enthält die Eigenschaftennamen und Werte für eine exportierte Element oder ein Element, das in einem Postfach hochgeladen werden soll. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ExportItems-Vorgang](exportitems-operation.md)
- [UploadItems-Vorgang](uploaditems-operation.md)

