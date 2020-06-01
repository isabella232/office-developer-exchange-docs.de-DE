---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: Das InternetMessageHeader-Element stellt den Internet Nachrichtenkopf für eine bestimmte Kopfzeile in der Headers-Auflistung dar. Verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS-und Internet Nachrichtenkopfzeilen, unterkauf-Internet Nachrichtenkopfzeilen in EWS, MIME und die fehlenden Internet Nachrichtenkopfzeilen.
ms.openlocfilehash: 7b662617e0b1a1fcdcce3449b729485ba6e0956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459307"
---
# <a name="internetmessageheader"></a><span data-ttu-id="1092e-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="1092e-105">InternetMessageHeader</span></span>

<span data-ttu-id="1092e-106">Das **InternetMessageHeader** -Element stellt den Internet Nachrichtenkopf für eine bestimmte Kopfzeile in der Headers-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="1092e-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="1092e-107">Verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1092e-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="1092e-108">Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Getting Internet Message Headers in [EWS, MIME, and the Missing Internet Message](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)Headers.</span><span class="sxs-lookup"><span data-stu-id="1092e-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="1092e-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="1092e-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1092e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1092e-110">Attributes and elements</span></span>

<span data-ttu-id="1092e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1092e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1092e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1092e-112">Attributes</span></span>

|<span data-ttu-id="1092e-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1092e-113">**Attribute**</span></span>|<span data-ttu-id="1092e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1092e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1092e-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="1092e-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="1092e-116">Gibt den Namen des Headers an.</span><span class="sxs-lookup"><span data-stu-id="1092e-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1092e-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1092e-117">Child elements</span></span>

<span data-ttu-id="1092e-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="1092e-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1092e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1092e-119">Parent elements</span></span>

|<span data-ttu-id="1092e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="1092e-120">**Element**</span></span>|<span data-ttu-id="1092e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1092e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1092e-122">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="1092e-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="1092e-123">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1092e-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1092e-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="1092e-124">Text value</span></span>

<span data-ttu-id="1092e-125">Der Wert Text stellt den Wert für den Header dar.</span><span class="sxs-lookup"><span data-stu-id="1092e-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1092e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1092e-126">Remarks</span></span>

<span data-ttu-id="1092e-127">Im folgenden finden Sie die verwaltete EWS-API erweiterte Eigenschaftsdefinition für die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1092e-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="1092e-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1092e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1092e-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1092e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1092e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1092e-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1092e-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1092e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1092e-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1092e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1092e-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1092e-133">Validation File</span></span>  <br/> |<span data-ttu-id="1092e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1092e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1092e-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1092e-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1092e-136">False</span><span class="sxs-lookup"><span data-stu-id="1092e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1092e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1092e-137">See also</span></span>



- [<span data-ttu-id="1092e-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1092e-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1092e-139">EWS, MIME und die fehlenden Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="1092e-139">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

