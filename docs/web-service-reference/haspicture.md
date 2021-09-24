---
title: HasPicture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HasPicture
api_type:
- schema
ms.assetid: 922a43fe-01bd-49f2-9261-e00e4699b8da
description: Das HasPicture-Element gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt.
ms.openlocfilehash: c00a51b5f43d951beb7325dbb6e10ae70ec94d04
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519527"
---
# <a name="haspicture"></a>HasPicture

Das **HasPicture-Element** gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt. 
  
[Contact](contact.md)
  
[HasPicture](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontaktperson](contact.md) <br/> |Stellt ein Kontaktelement im Exchange-Speicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **HasPicture-Elements** kann **"true"** oder **"false" sein.** Der Standardwert ist **false**.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

