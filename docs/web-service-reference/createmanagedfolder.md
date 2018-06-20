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
description: Das CreateManagedFolder-Element definiert eine Anforderung zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach.
ms.openlocfilehash: 4acc931de2a8665db092c3b309d914f0a3c67558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757792"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

Das **CreateManagedFolder** -Element definiert eine Anforderung zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach. 
  
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
|[FolderNames](foldernames.md) <br/> |Enthält ein Array von benannten verwaltete Ordner ein Postfach hinzu.  <br/> |
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Konto der Person ein, die die Anforderung stellt, muss FullAccess Berechtigungen für das Postfach verfügen, in dem die verwalteten Ordner erstellt werden. Parameters _ _ - AccessRights können mit dem Exchange-Verwaltungsshell- **Add-MailboxPermission** -Cmdlet Sie die Berechtigung FullAccess zuweisen. 
  
Obwohl Sie Exchange-Webdienste Hinzufügens von verwalteten Ordnern mit einem Postfach verwenden können, können Exchange-Webdienste Sie die Liste der verwalteten Ordner zugreifen, die verfügbar sind. Um eine Liste der verfügbaren verwalteten Ordner erhalten möchten, verwenden Sie das Cmdlet **Get-Managedfolder** Exchange-Verwaltungsshell. Verwalteten benutzerdefinierten Ordnern und verwalteten Standardordnern enthält die Liste, die vom **Cmdlet "Get-Managedfolder"** zurückgegeben wird. Sie können nur Ordner des Typs **Managedcustomfolder** an das Postfach mit der Operation CreateManagedFolder hinzufügen. 
  
> [!NOTE]
> Eine Liste der verwalteten Ordner erhalten mithilfe der API Verzeichnisdienste von Microsoft .NET Framework. 
  
Die [FindFolder Vorgang](findfolder-operation.md) können Sie verwaltete Ordner in einem Postfach suchen. Verwaltete Ordner können unterschieden werden, indem Sie das [BaseShape](baseshape.md) -Element in der Anforderung auf AllProperties festlegen. Die Antwort enthält ein [ManagedFolderInformation](managedfolderinformation.md) -Element, um die verwalteten Ordner aus der Exchange-Speicherordner zu unterscheiden. Sie können verwaltete Ordnern auf dieselbe Weise löschen, andere Ordnertypen zu löschen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)
  
[FindFolder Operation](findfolder-operation.md)


[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

