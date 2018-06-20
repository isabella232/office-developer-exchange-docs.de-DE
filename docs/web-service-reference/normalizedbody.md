---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: Das NormalizedBody-Element gibt eine HTML-Darstellung der die Body-Eigenschaft eines Elements als Fragment, das in einem anderen HTML-Text eingefügt werden kann.
ms.openlocfilehash: 07c2176d2c8a7473c06b7e42f8bcbbe6670581ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830548"
---
# <a name="normalizedbody"></a><span data-ttu-id="2476b-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="2476b-103">NormalizedBody</span></span>

<span data-ttu-id="2476b-104">Das **NormalizedBody** -Element gibt eine HTML-Darstellung der die **Body** -Eigenschaft eines Elements als Fragment, das in einem anderen HTML-Text eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2476b-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="2476b-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="2476b-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2476b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2476b-106">Attributes and elements</span></span>

<span data-ttu-id="2476b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2476b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2476b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2476b-108">Attributes</span></span>

|<span data-ttu-id="2476b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2476b-109">**Attribute**</span></span>|<span data-ttu-id="2476b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2476b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2476b-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="2476b-111">BodyType</span></span>  <br/> |<span data-ttu-id="2476b-112">Gibt den Typ des Hauptteils an.</span><span class="sxs-lookup"><span data-stu-id="2476b-112">Indicates the body type.</span></span> <span data-ttu-id="2476b-113">Der Wert der **Text** für das **BodyType** -Attribut gibt an, dass der Text in nur-Text-Format ist.</span><span class="sxs-lookup"><span data-stu-id="2476b-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="2476b-114">Der Wert von **HTML** für das **BodyType** -Attribut gibt an, dass der Textkörper in HTML-Formular ist.</span><span class="sxs-lookup"><span data-stu-id="2476b-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="2476b-115">Das Attribut **BodyType** ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2476b-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="2476b-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="2476b-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="2476b-117">Gibt an, dass der Inhalt des Body abgeschnitten worden sein.</span><span class="sxs-lookup"><span data-stu-id="2476b-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="2476b-118">Der Textwert **false** für das **IsTruncated** -Attribut gibt an, dass der Inhalt des Body nicht abgeschnitten worden sein.</span><span class="sxs-lookup"><span data-stu-id="2476b-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="2476b-119">Normalisierte Textkörper werden abgeschnitten, wenn die normalisierte Textkörper Länge länger als der Wert im [MaximumBodySize](maximumbodysize.md) -Element festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2476b-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2476b-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2476b-120">Child elements</span></span>

<span data-ttu-id="2476b-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="2476b-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2476b-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2476b-122">Parent elements</span></span>

<span data-ttu-id="2476b-123">[Element](item.md) | [Nachricht](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Aufgabe](task.md) | [PostItem-Objekt ](postitem.md)  |  [CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="2476b-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2476b-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="2476b-124">Text value</span></span>

<span data-ttu-id="2476b-125">Der Textwert des **NormalizedBody** -Elements ist die normalisierte Textkörper des Elements.</span><span class="sxs-lookup"><span data-stu-id="2476b-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2476b-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2476b-126">Remarks</span></span>

<span data-ttu-id="2476b-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2476b-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2476b-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2476b-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2476b-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2476b-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2476b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="2476b-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2476b-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2476b-131">Schema name</span></span>  <br/> |<span data-ttu-id="2476b-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2476b-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="2476b-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2476b-133">Validation file</span></span>  <br/> |<span data-ttu-id="2476b-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2476b-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2476b-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2476b-135">Can be empty</span></span>  <br/> ||
   

