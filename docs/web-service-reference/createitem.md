---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: Das CreateItem-Element definiert eine Anforderung zum Erstellen eines Elements im Exchange Speicher.
ms.openlocfilehash: 7276b88bd3b90edc68d7ac8fd4a7646324eadb61
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526498"
---
# <a name="createitem"></a>CreateItem

Das **CreateItem-Element** definiert eine Anforderung zum Erstellen eines Elements im Exchange Speicher. 
  
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
|**MessageDisposition** <br/> |Beschreibt, wie das Element behandelt wird, nachdem es erstellt wurde. Das Attribut ist für E-Mail-Nachrichten erforderlich. Dieses Attribut gilt nur für E-Mail-Nachrichten.  <br/> |
|**SendMeetingInvitations** <br/> |Beschreibt, wie Besprechungsanfragen behandelt werden, nachdem sie erstellt wurden. Dieses Attribut ist für Kalenderelemente erforderlich.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition-Attribut

|Wert|Beschreibung|
|:-----|:-----|
|SaveOnly  <br/> |Das Nachrichtenelement wird in dem Ordner gespeichert, der vom [SavedItemFolderId-Element](saveditemfolderid.md) angegeben wird. Nachrichten können später mithilfe des [SendItem-Vorgangs](senditem-operation.md)gesendet werden. In der Antwort wird ein Elementbezeichner zurückgegeben. Elementbezeichner werden für keine Elementtypen zurückgegeben, mit Ausnahme von Nachrichtenelementen. Dies schließt Antwortobjekte ein.  <br/> |
|SendOnly  <br/> |Das Element wird gesendet, aber es wird keine Kopie im Ordner "Gesendete Elemente" gespeichert. Ein Elementbezeichner wird in der Antwort nicht zurückgegeben.<br/><br/>**HINWEIS:** **CreateItem** unterstützt keinen Delegatenzugriff, wenn die Option SendOnly verwendet wird, da mit dieser Option kein Zielordner angegeben werden kann. Die Problemumgehung besteht darin, das Element zu erstellen, den Elementbezeichner abzurufen und dann den SendItem-Vorgang zum Senden des Elements zu verwenden.           |
|SendAndSaveCopy  <br/> |Das Element wird gesendet, und eine Kopie wird in dem Ordner gespeichert, der durch das [SavedItemFolderId-Element](saveditemfolderid.md) identifiziert wird. Ein Elementbezeichner wird in der Antwort nicht zurückgegeben.<br/><br/>**HINWEIS:** Besprechungsanfragen werden nicht in dem Ordner gespeichert, der durch die [SavedItemFolderId-Eigenschaft](saveditemfolderid.md) identifiziert wird. Für kalendering, only the save location for calendar items can be specified by the **SavedItemFolderId** property. Sie können nicht steuern, wo ein Besprechungsanfrageelement gespeichert wird. Nur die zugeordneten Kalenderelemente werden kopiert und in dem Ordner gespeichert, der durch die **SavedItemFolderId-Eigenschaft** identifiziert wird.           |
   
#### <a name="sendmeetinginvitations-attribute"></a>SendMeetingInvitations-Attribut

|Wert|Beschreibung|
|:-----|:-----|
|SendToNone  <br/> |Wenn es sich bei dem Element um eine Besprechungsanfrage handelt, wird es als Kalenderelement gespeichert, aber nicht gesendet.  <br/> |
|SendOnlyToAll  <br/> |Die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendToAllAndSaveCopy  <br/> |Die Besprechungsanfrage wird an alle Teilnehmer gesendet, und eine Kopie wird in dem Ordner gespeichert, der vom [SavedItemFolderId-Element](saveditemfolderid.md) identifiziert wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|Element|Beschreibung|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Gibt den Zielordner an, in dem ein neues Element erstellt werden kann. Wenn das **MessageDisposition-Attribut** auf SendOnly festgelegt ist, wird nur eine erstellte Nachricht gesendet. Die Nachricht wird nicht in den Ordner eingefügt, der vom [SavedItemFolderId-Element](saveditemfolderid.md) identifiziert wird.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die im Ordner erstellt werden sollen, der durch das [SavedItemFolderId-Element](saveditemfolderid.md) identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateItemResponse](createitemresponse.md)  
- [CreateItem-Vorgang](createitem-operation.md)
- [Erstellen von E-Mail-Nachrichten](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [Erstellen von Terminen](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

