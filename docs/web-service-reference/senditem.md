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
description: Das SendItem-Element ist das Stammelement in einer Anforderung, ein Element im Exchange-Informationsspeicher zu senden.
ms.openlocfilehash: 28f0d484dd079146c998cb7317bd2d80c6739e19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530565"
---
# <a name="senditem"></a>SendItem

Das **SendItem** -Element ist das Stammelement in einer Anforderung, ein Element im Exchange-Informationsspeicher zu senden. 
  
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
|**SaveItemToFolder** <br/> |Gibt an, ob eine Kopie des gesendeten Elements gespeichert wird. Die Save-Aktion hängt vom Wert von **SaveItemToFolder** und davon ab, ob ein [SavedItemFolderId](saveditemfolderid.md) -Element in der Anforderung vorhanden ist. Dieses Element ist erforderlich.  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**true** <br/> |Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element nicht vorhanden ist, wird das Element im Ordner "Gesendete Elemente" gespeichert. Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element vorhanden ist, wird das Element in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element angegeben wird.  <br/> |
|**False** <br/> |Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element nicht vorhanden ist, wird das Element nicht gespeichert. Wenn das [SavedItemFolderId](saveditemfolderid.md) -Element vorhanden ist, wird eine Fehlerantwort mit einem [Response Code](responsecode.md) -Element zurückgegeben, das den **ErrorInvalidSendItemSaveSettings** -Wert enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn ein Element im Ordner "Gesendete Elemente" gesendet wird, wird das gesendete Element gelöscht, und eine Kopie davon wird im Ordner "Gesendete Elemente" abgelegt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SendItem-Vorgang](senditem-operation.md)

