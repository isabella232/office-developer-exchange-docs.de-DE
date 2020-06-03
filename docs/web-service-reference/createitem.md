---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: Das CreateItem-Element definiert eine Anforderung zum Erstellen eines Elements in der Exchange-Informationsspeicher.
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527061"
---
# <a name="createitem"></a>CreateItem

Das **CreateItem** -Element definiert eine Anforderung zum Erstellen eines Elements in der Exchange-Informationsspeicher. 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

**CreateItemType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|Attribut|Beschreibung|
|:-----|:-----|
|**MessageDisposition** <br/> |Beschreibt, wie das Element nach seiner Erstellung behandelt wird. Das Attribut ist für e-Mail-Nachrichten erforderlich. Dieses Attribut gilt nur für e-Mail-Nachrichten.  <br/> |
|**SendMeetingInvitations** <br/> |Beschreibt, wie Besprechungsanfragen verarbeitet werden, nachdem Sie erstellt wurden. Dieses Attribut ist für Kalenderelemente erforderlich.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition-Attribut

|Wert|Beschreibung|
|:-----|:-----|
|SaveOnly  <br/> |Das Nachrichtenelement wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element angegeben wird. Nachrichten können später mit dem SendItem- [Vorgang](senditem-operation.md)gesendet werden. In der Antwort wird ein Elementbezeichner zurückgegeben. Element-IDs werden nicht für Elementtypen mit Ausnahme von Nachrichtenelementen zurückgegeben. Dies umfasst Antwortobjekte.  <br/> |
|SendOnly  <br/> |Das Element wird gesendet, aber keine Kopie wird im Ordner "Gesendete Elemente" gespeichert. In der Antwort wird kein Elementbezeichner zurückgegeben.<br/><br/>**Hinweis**: **CreateItem** unterstützt keinen Stellvertretungszugriff, wenn die Option SendOnly verwendet wird, da ein Zielordner mit dieser Option nicht angegeben werden kann. Die Problemumgehung besteht darin, das Element zu erstellen, den Elementbezeichner abzurufen und dann mit dem SendItem-Vorgang das Element zu senden.           |
|SendAndSaveCopy  <br/> |Das Element wird gesendet, und eine Kopie wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird. In der Antwort wird kein Elementbezeichner zurückgegeben.<br/><br/>**Hinweis**: Besprechungsanfragen werden nicht in dem Ordner gespeichert, der von der [SavedItemFolderId](saveditemfolderid.md) -Eigenschaft angegeben wird. Bei Kalendern kann nur der Speicherort für Kalenderelemente von der **SavedItemFolderId** -Eigenschaft angegeben werden. Sie können nicht steuern, wo ein Besprechungsanfrage Element gespeichert wird. Nur die zugeordneten Kalenderelemente werden kopiert und in dem Ordner gespeichert, der von der **SavedItemFolderId** -Eigenschaft identifiziert wird.           |
   
#### <a name="sendmeetinginvitations-attribute"></a>SendMeetingInvitations-Attribut

|Wert|Beschreibung|
|:-----|:-----|
|SendToNone  <br/> |Wenn es sich bei dem Element um eine Besprechungsanfrage handelt, wird es als Kalenderelement gespeichert, aber nicht gesendet.  <br/> |
|SendOnlyToAll  <br/> |Die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendToAllAndSaveCopy  <br/> |Die Besprechungsanfrage wird an alle Teilnehmer gesendet, und eine Kopie wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|Element|Beschreibung|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Gibt den Zielordner an, in dem ein neues Element erstellt werden kann. Wenn das **MessageDisposition** -Attribut auf SendOnly festgelegt ist, wird nur eine erstellte Nachricht gesendet. Die Nachricht wird nicht in den Ordner eingefügt, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateItemResponse](createitemresponse.md)  
- [CreateItem-Vorgang](createitem-operation.md)
- [Erstellen von e-Mail-Nachrichten](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [Erstellen von Terminen](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

