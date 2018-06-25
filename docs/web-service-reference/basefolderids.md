---
title: BaseFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseFolderIds
api_type:
- schema
ms.assetid: bdaa6093-f960-469a-b338-0e75aaa536c6
description: Das Element BaseFolderIds stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen.
ms.openlocfilehash: 960e4d9c1d6eb37bf988bf163e696cbba3e1ef6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757424"
---
# <a name="basefolderids"></a>BaseFolderIds

Das Element **BaseFolderIds** stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen. 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert MicrosoftExchange Server 2007-Ordner, die nach Namen verwiesen werden können.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchParameters](searchparameters.md) <br/> |Stellt die Parameter, die einen Suchordner definieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **BaseFolderIds** -Element muss mindestens ein [FolderId](folderid.md) oder [DistinguishedFolderId](distinguishedfolderid.md) -Element enthalten. 
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

