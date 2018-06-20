---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: Das DiagnosticsLevel-Element darstellt, Timing und Leistungsinformationen, die verwendet wird, um den Bericht abgeleitet werden.
ms.openlocfilehash: 9205625bb6cf38e370e29d96770eb293ed9277f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757972"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="d5b9e-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="d5b9e-103">DiagnosticsLevel</span></span>

<span data-ttu-id="d5b9e-104">Das **DiagnosticsLevel** -Element darstellt, Timing und Leistungsinformationen, die verwendet wird, um den Bericht abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="d5b9e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d5b9e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5b9e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5b9e-106">Attributes and elements</span></span>

<span data-ttu-id="d5b9e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5b9e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5b9e-108">Attributes</span></span>

<span data-ttu-id="d5b9e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5b9e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5b9e-110">Child elements</span></span>

<span data-ttu-id="d5b9e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5b9e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5b9e-112">Parent elements</span></span>

|<span data-ttu-id="d5b9e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5b9e-113">**Element**</span></span>|<span data-ttu-id="d5b9e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5b9e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b9e-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d5b9e-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="d5b9e-116">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="d5b9e-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d5b9e-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="d5b9e-118">Enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d5b9e-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d5b9e-119">Text value</span></span>

<span data-ttu-id="d5b9e-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5b9e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5b9e-121">Remarks</span></span>

<span data-ttu-id="d5b9e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d5b9e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5b9e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d5b9e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5b9e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5b9e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5b9e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5b9e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d5b9e-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d5b9e-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5b9e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5b9e-127">Validation File</span></span>  <br/> |<span data-ttu-id="d5b9e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d5b9e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5b9e-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5b9e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5b9e-130">False</span><span class="sxs-lookup"><span data-stu-id="d5b9e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5b9e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5b9e-131">See also</span></span>

- [<span data-ttu-id="d5b9e-132">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5b9e-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="d5b9e-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d5b9e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

