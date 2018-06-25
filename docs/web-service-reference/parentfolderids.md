---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: Das ParentFolderIds-Element identifiziert Ordner für die FindItem und FindFolder Vorgänge zu suchen.
ms.openlocfilehash: 4dd23b45dcc397e29e67fc08b29dd773e50f0db1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830688"
---
# <a name="parentfolderids"></a>ParentFolderIds

Das **ParentFolderIds** -Element identifiziert Ordner für die FindItem und FindFolder Vorgänge zu suchen. 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
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
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners. Das **ParentFolderIds** -Element muss dieses Element oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element verwenden.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert die Microsoft Exchange Server 2007-Ordner, die nach Namen verwiesen werden können. Das **ParentFolderIds** -Element muss dieses Element oder die [FolderId](folderid.md) -Element verwenden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.  <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> |
|[ResolveNames](resolvenames.md) <br/> |Definiert eine Anforderung zum Auflösen von Names nicht eindeutig.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Element **ParentFolderIds** muss die [FolderId](folderid.md) oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element verwenden. Für die Suche kann eine unbegrenzte Anzahl von Ordnern definiert werden. 
  
## <a name="example"></a>Beispiel

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindFolder Operation](findfolder-operation.md)  
- [FindItem-Vorgang](finditem-operation.md) 
- [ResolveNames-Vorgang](resolvenames-operation.md)

