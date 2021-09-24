---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: Das CreateManagedFolder-Element definiert eine Anforderung zum Hinzufügen von verwalteten benutzerdefinierten Ordnern zu einem Postfach.
ms.openlocfilehash: ca6850cfdc8a37bf0480db0c040b035591a59ce6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536373"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

Das **CreateManagedFolder-Element** definiert eine Anforderung zum Hinzufügen von verwalteten benutzerdefinierten Ordnern zu einem Postfach. 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Konto der Person, die die Anforderung stellt, muss über FullAccess-Berechtigungen für das Postfach verfügen, in dem die verwalteten Ordner erstellt werden. Sie können den Parameter _-AccessRights _ mit dem Cmdlet Exchange Management Shell **Add-MailboxPermission** verwenden, um die Berechtigung FullAccess zuzuweisen. 
  
Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete Ordner hinzuzufügen, können Sie Exchange Webdienste nicht verwenden, um auf die Liste der verfügbaren verwalteten Ordner zuzugreifen. Verwenden Sie das Cmdlet **"get-managedfolder** Exchange Management Shell", um eine Liste der verfügbaren verwalteten Ordner abzurufen. Die Liste, die vom **Cmdlet "get-managedfolder"** zurückgegeben wird, enthält sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner. Sie können dem Postfach nur Mithilfe des CreateManagedFolder-Vorgangs Ordner vom Typ **"managedcustomfolder"** hinzufügen. 
  
> [!NOTE]
> Sie können auch eine Liste der verwalteten Ordner mithilfe der DirectoryServices-API des Microsoft .NET Framework abrufen. 
  
Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete Ordner in einem Postfach zu suchen. Verwaltete Ordner können unterschieden werden, indem das [BaseShape-Element](baseshape.md) in der Anforderung auf AllProperties festgelegt wird. Die Antwort enthält ein [ManagedFolderInformation-Element,](managedfolderinformation.md) um die verwalteten Ordner von den Exchange-Speicherordnern zu unterscheiden. Sie können verwaltete Ordner auf die gleiche Weise löschen wie andere Ordnertypen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)
  
[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

