---
title: EndDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateTime
api_type:
- schema
ms.assetid: 54d14e47-a8f7-400b-a859-c7ea7ce4c6a4
description: Das enddate-Element gibt das Enddatum und die Endzeit für eine Regel oder eine Suche an.
ms.openlocfilehash: 9556e4c1ef405ae66a71d19d99d9a71a61f54efc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460134"
---
# <a name="enddatetime"></a><span data-ttu-id="d8c6d-103">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d8c6d-103">EndDateTime</span></span>

<span data-ttu-id="d8c6d-104">Das **EndDate-Element gibt** das Enddatum und die Endzeit für eine Regel oder eine Suche an.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-104">The **EndDateTime** element specifies the end date and time for a rule or a search.</span></span> 
  
```XML
<EndDateTime/>
```

 <span data-ttu-id="d8c6d-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="d8c6d-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8c6d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d8c6d-106">Attributes and elements</span></span>

<span data-ttu-id="d8c6d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8c6d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d8c6d-108">Attributes</span></span>

<span data-ttu-id="d8c6d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8c6d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8c6d-110">Child elements</span></span>

<span data-ttu-id="d8c6d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8c6d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8c6d-112">Parent elements</span></span>

|<span data-ttu-id="d8c6d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8c6d-113">**Element**</span></span>|<span data-ttu-id="d8c6d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8c6d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8c6d-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d8c6d-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="d8c6d-116">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="d8c6d-117">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="d8c6d-117">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="d8c6d-118">Gibt den Datumsbereich an, innerhalb dessen eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-118">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8c6d-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d8c6d-119">Text value</span></span>

<span data-ttu-id="d8c6d-120">Ein Textwert, der eine Datum/Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-120">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8c6d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8c6d-121">Remarks</span></span>

<span data-ttu-id="d8c6d-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d8c6d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8c6d-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d8c6d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8c6d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8c6d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d8c6d-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d8c6d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d8c6d-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d8c6d-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d8c6d-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d8c6d-127">Validation File</span></span>  <br/> |<span data-ttu-id="d8c6d-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d8c6d-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d8c6d-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d8c6d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8c6d-130">False</span><span class="sxs-lookup"><span data-stu-id="d8c6d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8c6d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8c6d-131">See also</span></span>



- [<span data-ttu-id="d8c6d-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d8c6d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

