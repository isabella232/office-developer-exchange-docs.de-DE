---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: Das CreateManagedFolder-Element definiert eine Anforderung zum Hinzufügen verwalteter benutzerdefinierter Ordner zu einem Postfach.
ms.openlocfilehash: 01fe8b7341c38ad33089c56271434ad3f9a4e5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458362"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

Das **CreateManagedFolder** -Element definiert eine Anforderung zum Hinzufügen verwalteter benutzerdefinierter Ordner zu einem Postfach. 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 **CreateManagedFolderRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Enthält ein Array benannter verwalteter Ordner, die einem Postfach hinzugefügt werden sollen.  <br/> |
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Konto der Person, die die Anforderung macht, muss über FullAccess-Berechtigungen für das Postfach verfügen, in dem die verwalteten Ordner erstellt werden. Sie können den _-AccessRights _-Parameter mit dem Exchange-Verwaltungsshell **Add-MailboxPermission-** Cmdlet verwenden, um die FullAccess-Berechtigung zuzuweisen. 
  
Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete Ordner hinzuzufügen, können Sie Exchange Webdienste nicht verwenden, um auf die Liste der verfügbaren verwalteten Ordner zuzugreifen. Um eine Liste der verfügbaren verwalteten Ordner zu erhalten, verwenden Sie das Cmdlet **Get-ManagedFolder** Exchange-Verwaltungsshell. Die Liste, die vom **Cmdlet Get-ManagedFolder** zurückgegeben wird, enthält sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner. Sie können dem Postfach nur Ordner vom Typ **ManagedCustomFolder** hinzufügen, indem Sie den CreateManagedFolder-Vorgang verwenden. 
  
> [!NOTE]
> Sie können auch eine Liste der verwalteten Ordner abrufen, indem Sie die DirectoryServices-API des Microsoft .NET Framework verwenden. 
  
Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete Ordner in einem Postfach zu suchen. Verwaltete Ordner können unterschieden werden, indem das [BaseShape](baseshape.md) -Element auf allproperties in der Anforderung festgelegt wird. Die Antwort enthält ein [ManagedFolderInformation](managedfolderinformation.md) -Element, um die verwalteten Ordner von den Exchange-Informationsspeicher Ordnern zu unterscheiden. Sie können verwaltete Ordner auf die gleiche Weise löschen, wie Sie andere Ordnertypen löschen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)
  
[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

