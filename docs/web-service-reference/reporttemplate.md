---
title: Report Template
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: Das Report Template-Element stellt den Typ des abzurufenden Berichts dar.
ms.openlocfilehash: 22f14d326032a30e5cb4c2c9e1aff390d98e95e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528699"
---
# <a name="reporttemplate"></a><span data-ttu-id="26ff6-103">Report Template</span><span class="sxs-lookup"><span data-stu-id="26ff6-103">ReportTemplate</span></span>

<span data-ttu-id="26ff6-104">Das **Report Template** -Element stellt den Typ des abzurufenden Berichts dar.</span><span class="sxs-lookup"><span data-stu-id="26ff6-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="26ff6-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="26ff6-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26ff6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26ff6-106">Attributes and elements</span></span>

<span data-ttu-id="26ff6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="26ff6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26ff6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="26ff6-108">Attributes</span></span>

<span data-ttu-id="26ff6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="26ff6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26ff6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26ff6-110">Child elements</span></span>

<span data-ttu-id="26ff6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="26ff6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26ff6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26ff6-112">Parent elements</span></span>

|<span data-ttu-id="26ff6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26ff6-113">**Element**</span></span>|<span data-ttu-id="26ff6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26ff6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26ff6-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="26ff6-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="26ff6-116">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="26ff6-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26ff6-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="26ff6-117">Text value</span></span>

<span data-ttu-id="26ff6-118">In der folgenden Tabelle sind die möglichen Werte für das **Report Template** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="26ff6-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="26ff6-119">**Report Template-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="26ff6-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="26ff6-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="26ff6-120">**Value**</span></span>|<span data-ttu-id="26ff6-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26ff6-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26ff6-122">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="26ff6-122">Summary</span></span>  <br/> |<span data-ttu-id="26ff6-123">Gibt an, dass der Bericht alle Empfänger der Nachricht und den Zustellungsstatus der Nachricht für jeden Empfänger anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="26ff6-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="26ff6-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="26ff6-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="26ff6-125">Gibt an, dass der Bericht für einen einzelnen Empfänger einen vollständigen Verlauf der aufgetretenen Ereignisse anzeigt.</span><span class="sxs-lookup"><span data-stu-id="26ff6-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26ff6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26ff6-126">Remarks</span></span>

<span data-ttu-id="26ff6-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="26ff6-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26ff6-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="26ff6-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26ff6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="26ff6-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26ff6-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26ff6-130">Schema Name</span></span>  <br/> |<span data-ttu-id="26ff6-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="26ff6-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26ff6-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26ff6-132">Validation File</span></span>  <br/> |<span data-ttu-id="26ff6-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="26ff6-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26ff6-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26ff6-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="26ff6-135">False</span><span class="sxs-lookup"><span data-stu-id="26ff6-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26ff6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26ff6-136">See also</span></span>



- [<span data-ttu-id="26ff6-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="26ff6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

