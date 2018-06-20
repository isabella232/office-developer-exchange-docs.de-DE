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
description: Das InternetMessageHeader-Element darstellt, den Internet Nachrichtenkopf für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung. Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen, SeeGetting Internet-Nachrichtenköpfe in EWS MIME und fehlenden Internetkopfzeilen Nachricht.
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829952"
---
# <a name="internetmessageheader"></a><span data-ttu-id="abe5c-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="abe5c-105">InternetMessageHeader</span></span>

<span data-ttu-id="abe5c-106">Das **InternetMessageHeader** -Element darstellt, den Internet Nachrichtenkopf für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="abe5c-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="abe5c-107">Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="abe5c-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="abe5c-108">Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Nachrichtenkopfzeilen in [EWS, MIME, und die fehlenden Internet Nachrichtenkopfzeilen](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)Internet abrufen.</span><span class="sxs-lookup"><span data-stu-id="abe5c-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="abe5c-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="abe5c-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abe5c-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="abe5c-110">Attributes and elements</span></span>

<span data-ttu-id="abe5c-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="abe5c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abe5c-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="abe5c-112">Attributes</span></span>

|<span data-ttu-id="abe5c-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="abe5c-113">**Attribute**</span></span>|<span data-ttu-id="abe5c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abe5c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abe5c-115">**HeaderName**</span><span class="sxs-lookup"><span data-stu-id="abe5c-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="abe5c-116">Gibt den Kopfzeilennamen.</span><span class="sxs-lookup"><span data-stu-id="abe5c-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abe5c-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abe5c-117">Child elements</span></span>

<span data-ttu-id="abe5c-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="abe5c-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="abe5c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abe5c-119">Parent elements</span></span>

|<span data-ttu-id="abe5c-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="abe5c-120">**Element**</span></span>|<span data-ttu-id="abe5c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abe5c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abe5c-122">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="abe5c-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="abe5c-123">Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="abe5c-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="abe5c-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="abe5c-124">Text value</span></span>

<span data-ttu-id="abe5c-125">Der Textwert steht für den Wert für die Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="abe5c-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abe5c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="abe5c-126">Remarks</span></span>

<span data-ttu-id="abe5c-127">Es folgt die EWS Managed API erweiterten Eigenschaftendefinition für die Eigenschaft **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="abe5c-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="abe5c-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="abe5c-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abe5c-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="abe5c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abe5c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="abe5c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abe5c-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="abe5c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="abe5c-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="abe5c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="abe5c-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="abe5c-133">Validation File</span></span>  <br/> |<span data-ttu-id="abe5c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abe5c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abe5c-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="abe5c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="abe5c-136">False</span><span class="sxs-lookup"><span data-stu-id="abe5c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abe5c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abe5c-137">See also</span></span>



- [<span data-ttu-id="abe5c-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="abe5c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="abe5c-139">EWS, MIME und die fehlenden Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="abe5c-139">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

