---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: Das SendItem-Element ist das Stammelement in einer Anforderung zum Senden eines Elements im Exchange Speicher.
ms.openlocfilehash: 2d1613451e7f876f0b612a3249570412e40b4764
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521620"
---
# <a name="senditem"></a>SendItem

Das **SendItem-Element** ist das Stammelement in einer Anforderung zum Senden eines Elements im Exchange Speicher. 
  
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
|**SaveItemToFolder** <br/> |Gibt an, ob eine Kopie des gesendeten Elements gespeichert wird. Die Speicheraktion hängt vom Wert von **SaveItemToFolder** und davon ab, ob ein [SavedItemFolderId-Element](saveditemfolderid.md) in der Anforderung vorhanden ist. Dieses Element ist erforderlich.  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**STIMMT** <br/> |Wenn das [SavedItemFolderId-Element](saveditemfolderid.md) nicht vorhanden ist, wird das Element im Ordner "Gesendete Elemente" gespeichert. Wenn das [SavedItemFolderId-Element](saveditemfolderid.md) vorhanden ist, wird das Element in dem Ordner gespeichert, der durch das [SavedItemFolderId-Element](saveditemfolderid.md) angegeben wird.  <br/> |
|**FALSE** <br/> |Wenn das [SavedItemFolderId-Element](saveditemfolderid.md) nicht vorhanden ist, wird das Element nicht gespeichert. Wenn das [SavedItemFolderId-Element](saveditemfolderid.md) vorhanden ist, wird eine Fehlerantwort mit einem [ResponseCode-Element](responsecode.md) zurückgegeben, das den **ErrorInvalidSendItemSaveSettings-Wert** enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Enthält die eindeutigen Identitäten von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die zum Löschen, Senden, Abrufen, Verschieben oder Kopieren von Elementen im Exchange Speicher verwendet werden.  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange Speicher aktualisieren, senden und erstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Element im Ordner "Gesendete Elemente" gesendet wird, wird das gesendete Element gelöscht, und eine Kopie davon wird im Ordner "Gesendete Elemente" abgelegt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SendItem-Vorgang](senditem-operation.md)

