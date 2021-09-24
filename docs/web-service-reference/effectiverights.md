---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: Das EffectiveRights-Element enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: a3207a9971065d3b69b6a0b7056fa8012425fd5b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514711"
---
# <a name="effectiverights"></a>EffectiveRights

Das **EffectiveRights-Element** enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt. 
  
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
|[CreateAssociated](createassociated.md) <br/> |Gibt an, ob ein Client ein zugeordnetes Inhaltsverzeichnis erstellen kann. Diese Eigenschaft wird nur für Ordnerobjekte verwendet.  <br/> |
|[CreateContents](createcontents.md) <br/> |Gibt an, ob ein Client ein Inhaltsverzeichnis erstellen kann. Diese Eigenschaft wird nur für Ordnerobjekte verwendet.  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |Gibt an, ob ein Client eine Hierarchietabelle erstellen kann. Diese Eigenschaft wird nur für Ordnerobjekte verwendet.  <br/> |
|[Löschen](delete.md) <br/> |Gibt an, ob ein Client einen Ordner oder ein Element löschen kann.  <br/> |
|[Modify](modify.md) <br/> |Gibt an, ob ein Client einen Ordner oder ein Element ändern kann.  <br/> |
|[Lesen](read.md) <br/> |Gibt an, ob ein Client einen Ordner oder ein Element lesen kann.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Gibt an, ob ein privates Element angezeigt werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach dar.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontaktordner in einem Postfach dar.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach dar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Aspekt](item.md) <br/> |Stellt ein generisches Exchange Element dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Beitragselement im Exchange Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

**EffectiveRights** wird in den Antworten GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy und SyncFolderItems unterstützt. Die **EffectiveRights-Eigenschaft** wird im **AllProperties-Shape** für Ordner und Elemente verfügbar gemacht. 
  
Diese **EffectiveRights-Eigenschaft** ermöglicht den Zugriff auf dieselben Informationen, die in der **PR_ACCESS MAPI-Eigenschaft** bereitgestellt werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

