---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: Das FolderName-Element identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll.
ms.openlocfilehash: 76263d56c423411a58ea45d691ce93e2b3202571
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511565"
---
# <a name="foldername"></a>FolderName

Das **FolderName-Element** identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll. 
  
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

Ein Textwert ist erforderlich. Der Textwert stellt einen Ordnernamen dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete benutzerdefinierte Ordner hinzuzufügen, können Sie nicht dieselbe Technologie verwenden, um auf die Liste der verfügbaren verwalteten benutzerdefinierten Ordner zuzugreifen. Sie können eine Liste der verwalteten benutzerdefinierten Ordner mithilfe eines Befehls Exchange Verwaltungsshell oder mithilfe einer API abrufen, die mit dem Active Directory-Verzeichnisdienst verbunden ist. Der Ordnername ist der Name des entsprechenden Active Directory-Objekts.
  
Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete benutzerdefinierte Ordner zu suchen. Verwenden Sie den [DeleteFolder-Vorgang,](deletefolder-operation.md) um verwaltete benutzerdefinierte Ordner zu löschen. 
  
Es ist wichtig zu beachten, dass **FolderName** der Name eines vorhandenen verwalteten benutzerdefinierten Ordners in der Organisation ist. Der Versuch, einen Ordner hinzuzufügen, der sich nicht in der Organisation befindet, führt zu einer Fehlerantwort. 
  
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

