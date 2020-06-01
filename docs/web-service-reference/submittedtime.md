---
title: Übermittelt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmittedTime
api_type:
- schema
ms.assetid: 45c8fa36-c539-42ca-99dc-1ac33cc54afc
description: Das übermittelte Time-Element stellt die Uhrzeit dar, zu der die Nachricht in den Server eingegeben wurde.
ms.openlocfilehash: bf9495aa700d2887d199eccb38289e0ebd2e8636
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465408"
---
# <a name="submittedtime"></a><span data-ttu-id="ac254-103">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="ac254-103">SubmittedTime</span></span>

<span data-ttu-id="ac254-104">Das über **mittelte** Time-Element stellt die Uhrzeit dar, zu der die Nachricht in den Server eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ac254-104">The **SubmittedTime** element represents the time that the message entered the server.</span></span> 
  
```XML
<SubmittedTime/>
```

 <span data-ttu-id="ac254-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac254-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac254-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac254-106">Attributes and elements</span></span>

<span data-ttu-id="ac254-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac254-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac254-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac254-108">Attributes</span></span>

<span data-ttu-id="ac254-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac254-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac254-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac254-110">Child elements</span></span>

<span data-ttu-id="ac254-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac254-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac254-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac254-112">Parent elements</span></span>

|<span data-ttu-id="ac254-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac254-113">**Element**</span></span>|<span data-ttu-id="ac254-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac254-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac254-115">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="ac254-115">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="ac254-116">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ac254-116">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac254-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ac254-117">Text value</span></span>

 <span data-ttu-id="ac254-118">Ein Textwert, der eine Datum/Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac254-118">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ac254-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac254-119">Remarks</span></span>

<span data-ttu-id="ac254-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ac254-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac254-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac254-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac254-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac254-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac254-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac254-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ac254-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ac254-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac254-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac254-125">Validation File</span></span>  <br/> |<span data-ttu-id="ac254-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac254-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac254-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac254-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac254-128">False</span><span class="sxs-lookup"><span data-stu-id="ac254-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac254-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac254-129">See also</span></span>



- [<span data-ttu-id="ac254-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac254-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

