---
title: Übermittlungs Zeitangabe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmitTime
api_type:
- schema
ms.assetid: 97e4b71e-f45c-4bdb-80f9-805934916c0f
description: Das Submit Time-Element stellt die Uhrzeit dar, zu der die Nachricht an den Server gesendet wurde.
ms.openlocfilehash: e4409d962988ee308e0c0b461f9448ef68067fe8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467053"
---
# <a name="submittime"></a><span data-ttu-id="c1dee-103">Übermittlungs Zeitangabe</span><span class="sxs-lookup"><span data-stu-id="c1dee-103">SubmitTime</span></span>

<span data-ttu-id="c1dee-104">Das **Submit** Time-Element stellt die Uhrzeit dar, zu der die Nachricht an den Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c1dee-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="c1dee-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="c1dee-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1dee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1dee-106">Attributes and elements</span></span>

<span data-ttu-id="c1dee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1dee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1dee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1dee-108">Attributes</span></span>

<span data-ttu-id="c1dee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1dee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1dee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1dee-110">Child elements</span></span>

<span data-ttu-id="c1dee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1dee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1dee-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1dee-112">Parent elements</span></span>

|<span data-ttu-id="c1dee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1dee-113">**Element**</span></span>|<span data-ttu-id="c1dee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1dee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1dee-115">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c1dee-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="c1dee-116">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1dee-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1dee-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1dee-117">Text value</span></span>

<span data-ttu-id="c1dee-118">Ein Textwert, der eine Datum/Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1dee-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1dee-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1dee-119">Remarks</span></span>

<span data-ttu-id="c1dee-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1dee-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1dee-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1dee-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1dee-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1dee-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1dee-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1dee-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c1dee-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1dee-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1dee-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1dee-125">Validation File</span></span>  <br/> |<span data-ttu-id="c1dee-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1dee-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1dee-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1dee-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1dee-128">False</span><span class="sxs-lookup"><span data-stu-id="c1dee-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1dee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1dee-129">See also</span></span>



[<span data-ttu-id="c1dee-130">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c1dee-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="c1dee-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1dee-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

