---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: Das FindFolder-Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.
ms.openlocfilehash: 248047206a661afe723543e52c51b57847148423
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462577"
---
# <a name="findfolder"></a>FindFolder

Das **FindFolder** -Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach. 
  
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
|Traversal  <br/> |Definiert, wie eine Suche durchgeführt wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Weist den FindFolder-Vorgang an, nur den identifizierten Ordner zu durchsuchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden. Dies wird als flacher Durchlauf bezeichnet.  <br/> |
|Tiefe  <br/> |Weist den FindFolder-Vorgang an, in allen untergeordneten Ordnern des identifizierten übergeordneten Ordners zu suchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden. Dies wird als Deep Traversal bezeichnet.  <br/> |
|SoftDeleted  <br/> |Weist den FindFolder-Vorgang an, eine flache Durchquerung der Suche nach gelöschten Elementen durchzuführen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Gibt die Ordner Eigenschaften an, die in eine FindFolder-Antwort eingeschlossen werden sollen.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Beschreibt, wie Informationen zum ausgelagerten Element in einer FindFolder-Antwort zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Beschreibt, wo die ausgelagerte Ansicht beginnt und wie viele Ordner in einer FindFolder-Anforderung maximal zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[Einschränkung](restriction.md) <br/> |Definiert eine Einschränkung oder Abfrage, die zum Filtern von Ordnern in einem FindFolder-Vorgang verwendet wird. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifiziert Ordner für den zu durchsuchenden FindFolder-Vorgang.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer FindFolder-Anforderung wird gezeigt, wie eine Anforderung zum Auffinden aller Ordner in einem Posteingang bildet.
  
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
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindFolder-Vorgang](findfolder-operation.md)

