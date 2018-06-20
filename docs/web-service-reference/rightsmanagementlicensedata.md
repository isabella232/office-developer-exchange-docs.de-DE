---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: Das RightsManagementLicenseData-Element gibt Informationen zu den Rights Management-Lizenz für ein Element.
ms.openlocfilehash: ec2ba1dc155afe239c499246095f86fc621910a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831234"
---
# <a name="rightsmanagementlicensedata"></a><span data-ttu-id="dcd85-103">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="dcd85-103">RightsManagementLicenseData</span></span>

<span data-ttu-id="dcd85-104">Das **RightsManagementLicenseData** -Element gibt Informationen zu den Rights Management-Lizenz für ein Element.</span><span class="sxs-lookup"><span data-stu-id="dcd85-104">The **RightsManagementLicenseData** element specifies information about the rights management license for an item.</span></span> 
  
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

 <span data-ttu-id="dcd85-105">**RightsManagementLicenseDataType**</span><span class="sxs-lookup"><span data-stu-id="dcd85-105">**RightsManagementLicenseDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dcd85-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dcd85-106">Attributes and elements</span></span>

<span data-ttu-id="dcd85-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dcd85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcd85-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dcd85-108">Attributes</span></span>

<span data-ttu-id="dcd85-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dcd85-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dcd85-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcd85-110">Child elements</span></span>

<span data-ttu-id="dcd85-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [' RMSTemplateID '](rmstemplateid.md) | [TemplateName](templatename.md) | [TemplateDescription](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md)  |  [ ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md)  |  [ ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span><span class="sxs-lookup"><span data-stu-id="dcd85-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [RMSTemplateId](rmstemplateid.md) | [TemplateName](templatename.md) | [TemplateDescription](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md) | [ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md) | [ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dcd85-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcd85-112">Parent elements</span></span>

<span data-ttu-id="dcd85-113">[Element](item.md) | [Nachricht](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Aufgabe](task.md) | [PostItem-Objekt ](postitem.md)  |  [CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="dcd85-113">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dcd85-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcd85-114">Remarks</span></span>

<span data-ttu-id="dcd85-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dcd85-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dcd85-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dcd85-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dcd85-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dcd85-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcd85-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcd85-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dcd85-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dcd85-119">Schema name</span></span>  <br/> |<span data-ttu-id="dcd85-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dcd85-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="dcd85-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dcd85-121">Validation file</span></span>  <br/> |<span data-ttu-id="dcd85-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dcd85-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dcd85-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dcd85-123">Can be empty</span></span>  <br/> ||
   

