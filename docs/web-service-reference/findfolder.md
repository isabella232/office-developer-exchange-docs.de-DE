---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: Das FindFolder-Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.
ms.openlocfilehash: 431efde28e417efec04f6fa1625a81b3766cb705
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518442"
---
# <a name="findfolder"></a>FindFolder

Das **FindFolder-Element** definiert eine Anforderung zum Suchen von Ordnern in einem Postfach. 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

**FindFolderType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Traversal  <br/> |Definiert, wie eine Suche ausgeführt wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversalattributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Weist den FindFolder-Vorgang an, nur den identifizierten Ordner zu durchsuchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden. Dies wird als flaches Traversal bezeichnet.  <br/> |
|Tief  <br/> |Weist den FindFolder-Vorgang an, in allen untergeordneten Ordnern des angegebenen übergeordneten Ordners zu suchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden. Dies wird als deep traversal bezeichnet.  <br/> |
|Vorläufig gelöscht  <br/> |Weist den FindFolder-Vorgang an, eine flache Traversalsuche nach gelöschten Elementen durchzuführen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifiziert die Ordnereigenschaften, die in eine FindFolder-Antwort eingeschlossen werden sollen.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Beschreibt, wie Seitenelementinformationen in einer FindFolder-Antwort zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Beschreibt, wo die seitenierte Ansicht beginnt, und die maximale Anzahl von Ordnern, die in einer FindFolder-Anforderung zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[Restriction](restriction.md) <br/> |Definiert eine Einschränkung oder Abfrage, die zum Filtern von Ordnern in einem FindFolder-Vorgang verwendet wird. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifies folders for the FindFolder operation to search.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel einer FindFolder-Anforderung zeigt, wie Sie eine Anforderung zum Suchen aller Ordner in einem Posteingang erstellen.
  
```xml
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

