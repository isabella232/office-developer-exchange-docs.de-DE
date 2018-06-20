---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: Das DisableAppResponse-Element gibt die Antwort auf eine DisableApp an.
ms.openlocfilehash: 740801fa4b60e217f0b9148bcfcc5b206e96bf31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758007"
---
# <a name="disableappresponse"></a><span data-ttu-id="484bb-103">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="484bb-103">DisableAppResponse</span></span>

<span data-ttu-id="484bb-104">Das **DisableAppResponse** -Element gibt die Antwort auf eine **DisableApp** an.</span><span class="sxs-lookup"><span data-stu-id="484bb-104">The **DisableAppResponse** element specifies the response to a **DisableApp** request.</span></span> 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 <span data-ttu-id="484bb-105">**DisableAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="484bb-105">**DisableAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="484bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="484bb-106">Attributes and elements</span></span>

<span data-ttu-id="484bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="484bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="484bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="484bb-108">Attributes</span></span>

<span data-ttu-id="484bb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="484bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="484bb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="484bb-110">Child elements</span></span>

|<span data-ttu-id="484bb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="484bb-111">**Element**</span></span>|<span data-ttu-id="484bb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="484bb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="484bb-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="484bb-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="484bb-114">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="484bb-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="484bb-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="484bb-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="484bb-116">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="484bb-116">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="484bb-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="484bb-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="484bb-118">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="484bb-118">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="484bb-119">MessageXml</span><span class="sxs-lookup"><span data-stu-id="484bb-119">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="484bb-120">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="484bb-120">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="484bb-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="484bb-121">Parent elements</span></span>

<span data-ttu-id="484bb-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="484bb-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="484bb-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="484bb-123">Remarks</span></span>

<span data-ttu-id="484bb-124">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="484bb-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="484bb-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="484bb-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="484bb-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="484bb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="484bb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="484bb-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="484bb-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="484bb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="484bb-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="484bb-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="484bb-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="484bb-130">Validation File</span></span>  <br/> |<span data-ttu-id="484bb-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="484bb-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="484bb-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="484bb-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="484bb-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="484bb-133">See also</span></span>

- [<span data-ttu-id="484bb-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="484bb-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

