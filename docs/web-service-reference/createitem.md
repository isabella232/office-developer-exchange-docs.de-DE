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
description: Das CreateItem-Element definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.
ms.openlocfilehash: bb5cddd5ea4fa1b73c424275a0b0219ce3e189e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757782"
---
# <a name="createitem"></a>CreateItem

Das **CreateItem** -Element definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher. 
  
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

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**"MessageDisposition"** <br/> |Beschreibt, wie das Element behandelt werden sollen, nachdem er erstellt wurde. Das Attribut ist erforderlich, damit e-Mail-Nachrichten. Dieses Attribut gilt nur für e-mail-Nachrichten.  <br/> |
|**"SendMeetingInvitations"** <br/> |Beschreibt, wie Besprechungsanfragen behandelt werden, nachdem sie erstellt wurden. Dieses Attribut ist für Kalenderelemente erforderlich.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Attribut "MessageDisposition"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SaveOnly  <br/> |Das Nachrichten-Element wird im Ordner gespeichert, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) angegeben ist. Nachrichten können später gesendet werden, mit der [den SendItem-Vorgang](senditem-operation.md). Eine Element-ID wird in der Antwort zurückgegeben. Element-IDs werden für alle Elementtypen außer Nachrichtenelemente nicht zurückgegeben. Dazu gehören Antwortobjekte.  <br/> |
|SendOnly  <br/> |Das Element wird gesendet, jedoch keine Kopie im Ordner "Gesendete Elemente" gespeichert ist. Eine Element-ID wird nicht in der Antwort zurückgegeben.  <br/> > [!NOTE]> **CreateItem** unterstützt keine Zugriffsrechte für Stellvertretung, wenn die Option SendOnly verwendet wird, da mit dieser Option ein Zielordner angegeben werden kann. Die problemumgehung besteht darin, das Element erstellen, der Element-ID abgerufen, und klicken Sie dann den SendItem-Vorgang verwenden, um das Element gesendet.           |
|SendAndSaveCopy  <br/> |Das Element wird gesendet, und eine Kopie in den Ordner, der durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird. Eine Element-ID wird nicht in der Antwort zurückgegeben.  <br/> > [!NOTE]> Besprechungsanfragen werden nicht in den Ordner gespeichert, die von der [SavedItemFolderId](saveditemfolderid.md) -Eigenschaft angegeben wird. Für Kalenderfunktionen, nur das Speichern des Speicherorts für Kalenderelemente von der **SavedItemFolderId** -Eigenschaft angegeben werden kann. Sie können nicht steuern, auf dem eine Besprechungsanfrage Element gespeichert wird. Nur die zugeordneten Kalenderelemente werden kopiert und in den Ordner, der die **SavedItemFolderId** -Eigenschaft identifizierte gespeichert.           |
   
#### <a name="sendmeetinginvitations-attribute"></a>Attribut "SendMeetingInvitations"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Wenn das Element eine Besprechungsanfrage ist, wird es als ein Kalenderelement gespeichert, aber nicht gesendet.  <br/> |
|SendOnlyToAll  <br/> |Die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendToAllAndSaveCopy  <br/> |Senden von Besprechungsanfragen an alle Teilnehmer und eine Kopie in den Ordner, der durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Des SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner, in dem ein neues Element erstellt werden können. Wenn das Attribut **"MessageDisposition"** auf SendOnly festgelegt ist, wird nur eine erstellte Nachricht gesendet werden. Die Nachricht wird nicht im Ordner versetzt werden, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateItemResponse](createitemresponse.md)
  
[CreateItem Operation](createitem-operation.md)
  
 **CreateItemType**


[Erstellen von e-Mail-Nachrichten](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx)
  
[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Erstellen von Aufgaben](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Erstellen von Terminen](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

