---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: Das SendItem-Element ist das Stammelement im eine Anforderung zum Senden eines Elements im Exchange-Speicher.
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831340"
---
# <a name="senditem"></a>SendItem

Das **SendItem** -Element ist das Stammelement im eine Anforderung zum Senden eines Elements im Exchange-Speicher. 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |Bestimmt, ob eine Kopie der das gesendete Element gespeichert wird. Speichern in Aktion hängt vom Wert der **SaveItemToFolder** und gibt an, ob ein Element [des SavedItemFolderId](saveditemfolderid.md) in der Anforderung vorhanden ist. Dieses Element ist erforderlich.  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder-Attributs

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**"true"** <br/> |Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) nicht vorhanden ist, wird das Element im Ordner "Gesendete Elemente" gespeichert. Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) vorhanden ist, wird das Element im Ordner gespeichert, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) angegeben ist.  <br/> |
|**false** <br/> |Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) nicht vorhanden ist, wird das Element nicht gespeichert. Wenn das Element [des SavedItemFolderId](saveditemfolderid.md) vorhanden ist, wird eine Fehlerantwort mit einem [ResponseCode](responsecode.md) -Element zurückgegeben werden soll, die den **ErrorInvalidSendItemSaveSettings** -Wert enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Artikelnummern ein.](itemids.md) <br/> |Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.  <br/> |
|[Des SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn ein Element im Ordner "Gesendete Elemente" gesendet wird, wird das gesendete Element gelöscht, und eine Kopie davon hört im Ordner "Gesendete Elemente".
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SendItem Operation](senditem-operation.md)

