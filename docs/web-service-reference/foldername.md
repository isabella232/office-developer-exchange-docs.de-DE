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
description: Das FolderName-Element identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll.
ms.openlocfilehash: 1bb63e50c06e81337d1142a6624213fb2db12457
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461352"
---
# <a name="foldername"></a>FolderName

Das **FolderName** -Element identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Enthält ein Array benannter verwalteter benutzerdefinierter Ordner, die einem Postfach hinzugefügt werden sollen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert Text stellt einen Ordnernamen dar.
  
## <a name="remarks"></a>Bemerkungen

Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete benutzerdefinierte Ordner hinzuzufügen, können Sie nicht dieselbe Technologie für den Zugriff auf die Liste der verfügbaren verwalteten benutzerdefinierten Ordner verwenden. Sie können eine Liste verwalteter benutzerdefinierter Ordner abrufen, indem Sie einen Exchange-Verwaltungsshell-Befehl verwenden oder eine API verwenden, die mit dem Active Directory-Verzeichnisdienst Schnittstellen. Der Ordnername ist der Name des entsprechenden Active Directory-Objekts.
  
Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete benutzerdefinierte Ordner zu suchen. Verwenden Sie den [DeleteFolder-Vorgang](deletefolder-operation.md) , um verwaltete benutzerdefinierte Ordner zu löschen. 
  
Es ist wichtig zu beachten, dass **FolderName** der Name eines vorhandenen verwalteten benutzerdefinierten Ordners in der Organisation ist. Ein Versuch, einen Ordner hinzuzufügen, der nicht in der Organisation liegt, führt zu einer Fehlermeldung. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

