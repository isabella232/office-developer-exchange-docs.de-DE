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
description: Das DiagnosticsLevel-Element stellt Timing-und Leistungsinformationen dar, die zum Ableiten des Berichts verwendet werden.
ms.openlocfilehash: 3060d4f1b8449a5870d964bdfcdbf0d503905abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467830"
---
# <a name="diagnosticslevel"></a><span data-ttu-id="c0da0-103">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="c0da0-103">DiagnosticsLevel</span></span>

<span data-ttu-id="c0da0-104">Das **DiagnosticsLevel** -Element stellt Timing-und Leistungsinformationen dar, die zum Ableiten des Berichts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0da0-104">The **DiagnosticsLevel** element represents timing and performance information that will be used to derive the report.</span></span> 
  
```XML
<DiagnosticsLevel/>
```

 <span data-ttu-id="c0da0-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c0da0-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0da0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0da0-106">Attributes and elements</span></span>

<span data-ttu-id="c0da0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0da0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0da0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0da0-108">Attributes</span></span>

<span data-ttu-id="c0da0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0da0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0da0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0da0-110">Child elements</span></span>

<span data-ttu-id="c0da0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0da0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0da0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0da0-112">Parent elements</span></span>

|<span data-ttu-id="c0da0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0da0-113">**Element**</span></span>|<span data-ttu-id="c0da0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0da0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0da0-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c0da0-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="c0da0-116">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="c0da0-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="c0da0-117">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c0da0-117">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="c0da0-118">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="c0da0-118">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0da0-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c0da0-119">Text value</span></span>

<span data-ttu-id="c0da0-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0da0-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0da0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0da0-121">Remarks</span></span>

<span data-ttu-id="c0da0-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c0da0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0da0-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c0da0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0da0-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0da0-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0da0-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0da0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c0da0-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c0da0-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0da0-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0da0-127">Validation File</span></span>  <br/> |<span data-ttu-id="c0da0-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c0da0-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0da0-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0da0-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0da0-130">False</span><span class="sxs-lookup"><span data-stu-id="c0da0-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0da0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0da0-131">See also</span></span>

- [<span data-ttu-id="c0da0-132">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c0da0-132">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="c0da0-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c0da0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

