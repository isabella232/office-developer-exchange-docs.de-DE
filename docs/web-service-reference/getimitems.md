---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: Das GetImItems-Anforderungselement definiert eine Anforderung zum Abrufen von Informationen zu den angegebenen Chatgruppen und Chatkontaktpersonas.
ms.openlocfilehash: 99be8e898623b5bc8c517886132b77da40a7fb1e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513591"
---
# <a name="getimitems"></a>GetImItems

Das **GetImItems-Anforderungselement** definiert eine Anforderung zum Abrufen von Informationen zu den angegebenen Chatgruppen und Chatkontaktpersonas. 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 **GetImItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ContactIds](contactids.md)  |  [GroupIds](groupids.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

