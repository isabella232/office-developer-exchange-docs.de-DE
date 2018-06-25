---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: FolderName-Element gibt einen einzelnen verwalteten benutzerdefinierten Ordner ein Postfach hinzu.
ms.openlocfilehash: 56a7a7d256624c5103c88a333222807519d21501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758513"
---
# <a name="foldername"></a>FolderName

**FolderName** -Element gibt einen einzelnen verwalteten benutzerdefinierten Ordner ein Postfach hinzu. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[Ordnername](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Enthält ein Array von benannten verwalteten benutzerdefinierten Ordnern an ein Postfach hinzufügen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt einen Ordnernamen.
  
## <a name="remarks"></a>Hinweise

Obwohl Sie Exchange-Webdienste zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach verwenden können, können die gleiche Technologie Sie die Liste der verfügbaren verwalteten benutzerdefinierten Ordnern zugreifen. Sie können eine Liste der verwalteten benutzerdefinierten Ordnern abrufen, mit einer Exchange-Verwaltungsshell-Befehl oder mithilfe einer API, die Schnittstellen mit dem Active Directory-Verzeichnisdienst. Der Name des Ordners ist der Name des entsprechenden Active Directory-Objekts.
  
Die [FindFolder Vorgang](findfolder-operation.md) können Sie verwaltete benutzerdefinierte Ordnern suchen. Verwendung der [DeleteFolder-Vorgang](deletefolder-operation.md) zum Löschen verwalteten benutzerdefinierte Ordnern. 
  
Es ist wichtig, beachten Sie, dass der **Ordnername** der Name eines vorhandenen verwalteten benutzerdefinierten Ordners in der Organisation ist. Sie versuchen, einen Ordner hinzuzufügen, der nicht in der Organisation ist führt eine Fehlerantwort. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder Operation](findfolder-operation.md)


[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

