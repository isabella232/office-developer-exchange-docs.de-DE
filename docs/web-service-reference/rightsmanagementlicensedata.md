---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: Das RightsManagementLicenseData-Element gibt Informationen zur Rechteverwaltungslizenz für ein Element an.
ms.openlocfilehash: 8875e9bad425224f86b6de5149f87a36c2a2581e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523468"
---
# <a name="rightsmanagementlicensedata"></a>RightsManagementLicenseData

Das **RightsManagementLicenseData-Element** gibt Informationen zur Rechteverwaltungslizenz für ein Element an. 
  
```XML
<RightsManagementLicenseData>
   <RightsManagedMessageDecryptionStatus/>
   <RmsTemplateId/>
   <TemplateName/>
   <TemplateDescription/>
   <EditAllowed/>
   <ReplyAllowed/>
   <ReplyAllAllowed/>
   <ForwardAllowed/>
   <ModifyRecipientsAllowed/>
   <ExtractAllowed/>
   <PrintAllowed/>
   <ExportAllowed/>
   <ProgrammaticAccessAllowed/>
   <IsOwner/>
   <ContentOwner/>
   <ContentExpiryDate/>
</RightsManagementLicenseData>
```

 **RightsManagementLicenseDataType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md)  |  [RMSTemplateId](rmstemplateid.md)  |  [TemplateName](templatename.md)  |  [TemplateDescription](templatedescription.md)  |  [EditAllowed](editallowed.md)  |  [ReplyAllowed](replyallowed.md)  |  [ReplyAllAllowed](replyallallowed.md)  |  [ForwardAllowed](forwardallowed.md)  |  [ModifyRecipientsAllowed](modifyrecipientsallowed.md)  |  [ExtractAllowed](extractallowed.md)  |  [PrintAllowed](printallowed.md)  |  [ExportAllowed](exportallowed.md)  |  [ProgrammaticAccessAllowed](programmaticaccessallowed.md)  |  [IsOwner](isowner.md)  |  [ContentOwner](contentowner.md)  |  [ContentExpiryDate](contentexpirydate.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Aufgabe](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Kontakt](contact.md)  |  [DistributionList](distributionlist.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

