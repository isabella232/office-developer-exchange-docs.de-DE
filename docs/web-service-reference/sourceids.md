---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: Das SourceIds-Element enthält die zu konvertierenden Quellbezeichner.
ms.openlocfilehash: e6a0767de0928578fb6ae16996ff39908580d45c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521340"
---
# <a name="sourceids"></a>SourceIds

Das **SourceIds-Element** enthält die zu konvertierenden Quellbezeichner. 
  
[ConvertId](convertid.md)
  
[SourceIds](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 **NonEmptyArrayOfAlternateIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AlternateId](alternateid.md) <br/> |Beschreibt einen zu konvertierenden Element- oder Ordnerbezeichner.  <br/> |
|[AlternatePublicFolderId](alternatepublicfolderid.md) <br/> |Beschreibt einen zu konvertierenden Bezeichner für öffentliche Ordner.  <br/> |
|[AlternatePublicFolderItemId](alternatepublicfolderitemid.md) <br/> |Beschreibt einen zu konvertierenden Bezeichner für öffentliche Ordnerelemente.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConvertId](convertid.md) <br/> |Definiert eine Anforderung zum Konvertieren von Element- und Ordnerbezeichnern zwischen Exchange unterstützten Formaten.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ConvertId-Vorgang](convertid-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Konvertieren von Bezeichnern](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

