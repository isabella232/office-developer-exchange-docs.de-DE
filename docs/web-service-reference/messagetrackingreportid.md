---
title: MessageTrackingReportId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReportId
api_type:
- schema
ms.assetid: 9c604ca3-10fe-4760-b7fd-8b52f1a0c712
description: Das MessageTrackingReportId-Element stellt die Nachricht durch die Nachrichten-ID, die Organisation, in der die Nachricht gefunden wurde, den Server, auf dem die Nachricht gesendet wurde, und eine interne ID dar, die die Nachricht eindeutig identifiziert.
ms.openlocfilehash: d6e92593d55608e260634602c2aab694804d716d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460596"
---
# <a name="messagetrackingreportid"></a><span data-ttu-id="3e933-103">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="3e933-103">MessageTrackingReportId</span></span>

<span data-ttu-id="3e933-104">Das **MessageTrackingReportId** -Element stellt die Nachricht durch die Nachrichten-ID, die Organisation, in der die Nachricht gefunden wurde, den Server, auf dem die Nachricht gesendet wurde, und eine interne ID dar, die die Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3e933-104">The **MessageTrackingReportId** element represents the message by its message ID, the organization where the message was found, the server on which the message was submitted, and an internal ID that uniquely identifies the message.</span></span> 
  
```XML
<MessageTrackingReportId/>
```

 <span data-ttu-id="3e933-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="3e933-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e933-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e933-106">Attributes and elements</span></span>

<span data-ttu-id="3e933-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e933-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e933-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e933-108">Attributes</span></span>

<span data-ttu-id="3e933-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e933-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e933-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e933-110">Child elements</span></span>

<span data-ttu-id="3e933-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e933-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e933-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e933-112">Parent elements</span></span>

|<span data-ttu-id="3e933-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e933-113">**Element**</span></span>|<span data-ttu-id="3e933-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e933-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e933-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3e933-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="3e933-116">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="3e933-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="3e933-117">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="3e933-117">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="3e933-118">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="3e933-118">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3e933-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3e933-119">Text value</span></span>

<span data-ttu-id="3e933-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e933-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e933-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e933-121">Remarks</span></span>

<span data-ttu-id="3e933-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3e933-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e933-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e933-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e933-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e933-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e933-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e933-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3e933-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3e933-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e933-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e933-127">Validation File</span></span>  <br/> |<span data-ttu-id="3e933-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e933-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e933-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e933-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e933-130">False</span><span class="sxs-lookup"><span data-stu-id="3e933-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e933-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e933-131">See also</span></span>



[<span data-ttu-id="3e933-132">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3e933-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="3e933-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e933-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

