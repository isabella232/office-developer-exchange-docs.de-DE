---
title: GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: Das GetFolder-Element definiert eine Anforderung an einen Ordner aus einem Postfach im Exchange-Speicher abzurufen.
ms.openlocfilehash: 233da6ce57683350d4a13f6585593ac09438f0e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758681"
---
# <a name="getfolder"></a>GetFolder

Das **GetFolder** -Element definiert eine Anforderung an einen Ordner aus einem Postfach im Exchange-Speicher abzurufen. 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 **GetFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifiziert die Eigenschaften für jeden Ordner im [FolderIds](folderids.md) -Element identifiziert abgerufen.  <br/> |
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die verwendet werden, um Ordner zum Abrufen von einem Postfach im Exchange-Speicher zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFolder Operation](getfolder-operation.md)

