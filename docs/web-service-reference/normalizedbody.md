---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: Das NormalizedBody-Element gibt eine HTML-Darstellung der Body-Eigenschaft eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann.
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462668"
---
# <a name="normalizedbody"></a><span data-ttu-id="ea0c1-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="ea0c1-103">NormalizedBody</span></span>

<span data-ttu-id="ea0c1-104">Das **NormalizedBody** -Element gibt eine HTML-Darstellung der **Body** -Eigenschaft eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="ea0c1-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="ea0c1-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea0c1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ea0c1-106">Attributes and elements</span></span>

<span data-ttu-id="ea0c1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea0c1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea0c1-108">Attributes</span></span>

|<span data-ttu-id="ea0c1-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ea0c1-109">**Attribute**</span></span>|<span data-ttu-id="ea0c1-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ea0c1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea0c1-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="ea0c1-111">BodyType</span></span>  <br/> |<span data-ttu-id="ea0c1-112">Gibt den Typ des Texts an.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-112">Indicates the body type.</span></span> <span data-ttu-id="ea0c1-113">Der Wert des **Texts** für das **BodyType** -Attribut gibt an, dass sich der Textkörper in nur-Text-Form befindet.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="ea0c1-114">Der Wert von **HTML** für das **BodyType** -Attribut gibt an, dass sich der Text im HTML-Format befindet.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="ea0c1-115">Das **BodyType** -Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ea0c1-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="ea0c1-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="ea0c1-117">Gibt an, dass der Textkörper Inhalt abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="ea0c1-118">Der Textwert **false** für das Attribut **IsTruncated** gibt an, dass der Inhalt des Texts nicht abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="ea0c1-119">Der normalisierte Text wird abgeschnitten, wenn die normalisierte Körperlänge länger ist als der im [MaximumBodySize](maximumbodysize.md) -Element festgelegte Wert.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ea0c1-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea0c1-120">Child elements</span></span>

<span data-ttu-id="ea0c1-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ea0c1-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea0c1-122">Parent elements</span></span>

<span data-ttu-id="ea0c1-123">[Element](item.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Aufgabe](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="ea0c1-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ea0c1-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="ea0c1-124">Text value</span></span>

<span data-ttu-id="ea0c1-125">Der Textwert des **NormalizedBody** -Elements ist der normalisierte Text des Elements.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ea0c1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea0c1-126">Remarks</span></span>

<span data-ttu-id="ea0c1-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ea0c1-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ea0c1-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea0c1-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ea0c1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea0c1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea0c1-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ea0c1-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ea0c1-131">Schema name</span></span>  <br/> |<span data-ttu-id="ea0c1-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ea0c1-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="ea0c1-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ea0c1-133">Validation file</span></span>  <br/> |<span data-ttu-id="ea0c1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ea0c1-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ea0c1-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ea0c1-135">Can be empty</span></span>  <br/> ||
   

