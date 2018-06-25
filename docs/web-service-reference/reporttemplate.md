---
title: Berichtsvorlage
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
description: Das ReportTemplate-Element stellt den Typ des Berichts zu erhalten.
ms.openlocfilehash: 70aab69f4d20ad9fd7e878c7fccd16e261c9b94c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831118"
---
# <a name="reporttemplate"></a><span data-ttu-id="6f6d5-103">Berichtsvorlage</span><span class="sxs-lookup"><span data-stu-id="6f6d5-103">ReportTemplate</span></span>

<span data-ttu-id="6f6d5-104">Das **ReportTemplate** -Element stellt den Typ des Berichts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-104">The **ReportTemplate** element represents the type of report to get.</span></span> 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 <span data-ttu-id="6f6d5-105">**MessageTrackingReportTemplateType**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-105">**MessageTrackingReportTemplateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f6d5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6f6d5-106">Attributes and elements</span></span>

<span data-ttu-id="6f6d5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f6d5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f6d5-108">Attributes</span></span>

<span data-ttu-id="6f6d5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f6d5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f6d5-110">Child elements</span></span>

<span data-ttu-id="6f6d5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f6d5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f6d5-112">Parent elements</span></span>

|<span data-ttu-id="6f6d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-113">**Element**</span></span>|<span data-ttu-id="6f6d5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f6d5-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="6f6d5-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="6f6d5-116">Enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f6d5-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6f6d5-117">Text value</span></span>

<span data-ttu-id="6f6d5-118">Die folgende Tabelle enthält die möglichen Werte für das **ReportTemplate** -Element.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-118">The following table lists the possible values for the **ReportTemplate** element.</span></span> 
  
<span data-ttu-id="6f6d5-119">**ReportTemplate-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-119">**ReportTemplate element values**</span></span>

|<span data-ttu-id="6f6d5-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-120">**Value**</span></span>|<span data-ttu-id="6f6d5-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f6d5-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f6d5-122">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6f6d5-122">Summary</span></span>  <br/> |<span data-ttu-id="6f6d5-123">Gibt an, dass der Bericht alle Empfänger der Nachricht und den Zustellungsstatus der Nachricht auf jeden Empfänger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-123">Specifies that the report will display all the recipients of the message and the delivery status of the message to each recipient.</span></span>  <br/> |
|<span data-ttu-id="6f6d5-124">RecipientPath</span><span class="sxs-lookup"><span data-stu-id="6f6d5-124">RecipientPath</span></span>  <br/> |<span data-ttu-id="6f6d5-125">Gibt an, die für einen einzelnen Empfänger, wird der Bericht einen vollständigen Verlauf der Ereignisse angezeigt, die aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-125">Specifies that for a single recipient, the report will display a full history of the events that occurred.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f6d5-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f6d5-126">Remarks</span></span>

<span data-ttu-id="6f6d5-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6f6d5-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f6d5-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6f6d5-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f6d5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f6d5-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f6d5-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6f6d5-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6f6d5-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6f6d5-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f6d5-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6f6d5-132">Validation File</span></span>  <br/> |<span data-ttu-id="6f6d5-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f6d5-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f6d5-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6f6d5-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f6d5-135">False</span><span class="sxs-lookup"><span data-stu-id="6f6d5-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f6d5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f6d5-136">See also</span></span>



- [<span data-ttu-id="6f6d5-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f6d5-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

