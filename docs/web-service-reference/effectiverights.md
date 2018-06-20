---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: Das EffectiveRights-Element enthält den Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 610d9e214a8de648ece667799bb5e67dfcc358f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758146"
---
# <a name="effectiverights"></a>EffectiveRights

Das **EffectiveRights** -Element enthält den Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner. Dieses Element ist schreibgeschützt. 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 **EffectiveRightsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |Gibt an, ob ein Client eine zugeordnete Inhaltstabelle erstellen kann. Diese Eigenschaft wird nur auf Folder-Objekten verwendet.  <br/> |
|[CreateContents](createcontents.md) <br/> |Gibt an, ob ein Client eine Inhaltstabelle erstellen kann. Diese Eigenschaft wird nur auf Folder-Objekten verwendet.  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |Gibt an, ob ein Client eine Hierarchietabelle erstellen kann. Diese Eigenschaft wird nur auf Folder-Objekten verwendet.  <br/> |
|[Delete](delete.md) <br/> |Gibt an, ob ein Client eines Ordners oder Elements löschen kann.  <br/> |
|[Modify](modify.md) <br/> |Gibt an, ob ein Client eines Ordners oder Elements ändern kann.  <br/> |
|[Read](read.md) <br/> |Gibt an, ob ein Client eines Ordners oder Element lesen kann.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Gibt an, ob ein privates Element angezeigt werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach an.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner in einem Postfach an.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Exchange-Element.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[PostItem-Objekt](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Speicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

**EffectiveRights** wird in die Antworten GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy und SyncFolderItems unterstützt. Die **EffectiveRights** -Eigenschaft wird in der Form **AllProperties** für Ordner und Elemente verfügbar gemacht. 
  
Diese Eigenschaft **EffectiveRights** ermöglicht den Zugriff auf die gleichen Informationen, die in der **PR_ACCESS MAPI-** Eigenschaft bereitgestellt wird. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

