---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: Das ParentFolderIds-Element identifiziert Ordner für die Zu durchsuchenden FindItem- und FindFolder-Vorgänge.
ms.openlocfilehash: e9e0f14651b205ad64be04dbe1d0707a109f3edc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512905"
---
# <a name="parentfolderids"></a>ParentFolderIds

Das **ParentFolderIds-Element** identifiziert Ordner für die Zu durchsuchenden FindItem- und FindFolder-Vorgänge. 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

**NonEmptyArrayOfBaseFolderIdsType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners. Das **ParentFolderIds-Element** muss entweder dieses Element oder das [DistinguishedFolderId-Element](distinguishedfolderid.md) verwenden.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert Microsoft Exchange Server 2007-Ordner, auf die anhand des Namens verwiesen werden kann. Das **ParentFolderIds-Element** muss entweder dieses Element oder das [FolderId-Element](folderid.md) verwenden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.  <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> |
|[ResolveNames](resolvenames.md) <br/> |Definiert eine Anforderung zum Auflösen von mehrdeutigen Namen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **ParentFolderIds-Element** muss entweder die [FolderId](folderid.md) oder das [DistinguishedFolderId-Element](distinguishedfolderid.md) verwenden. Für die Suche kann eine unbegrenzte Anzahl von Ordnern definiert werden. 
  
## <a name="example"></a>Beispiel

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindFolder-Vorgang](findfolder-operation.md)  
- [FindItem-Vorgang](finditem-operation.md) 
- [ResolveNames-Vorgang](resolvenames-operation.md)

