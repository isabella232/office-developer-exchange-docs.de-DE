---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: Das DisableAppResponse-Element gibt die Antwort auf eine DisableApp-Anforderung an.
ms.openlocfilehash: cc28abf644247339e1226cd0e13824cc5f5669be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455646"
---
# <a name="disableappresponse"></a><span data-ttu-id="f9910-103">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="f9910-103">DisableAppResponse</span></span>

<span data-ttu-id="f9910-104">Das **DisableAppResponse** -Element gibt die Antwort auf eine **DisableApp** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f9910-104">The **DisableAppResponse** element specifies the response to a **DisableApp** request.</span></span> 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 <span data-ttu-id="f9910-105">**DisableAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="f9910-105">**DisableAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9910-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9910-106">Attributes and elements</span></span>

<span data-ttu-id="f9910-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9910-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9910-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9910-108">Attributes</span></span>

<span data-ttu-id="f9910-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9910-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9910-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9910-110">Child elements</span></span>

|<span data-ttu-id="f9910-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9910-111">**Element**</span></span>|<span data-ttu-id="f9910-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9910-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9910-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="f9910-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f9910-114">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="f9910-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f9910-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f9910-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f9910-116">Stellt Statusinformationen zur Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="f9910-116">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="f9910-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f9910-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f9910-118">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f9910-118">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="f9910-119">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="f9910-119">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f9910-120">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="f9910-120">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9910-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9910-121">Parent elements</span></span>

<span data-ttu-id="f9910-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9910-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9910-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9910-123">Remarks</span></span>

<span data-ttu-id="f9910-124">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f9910-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f9910-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f9910-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9910-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f9910-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9910-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9910-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9910-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9910-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f9910-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f9910-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="f9910-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9910-130">Validation File</span></span>  <br/> |<span data-ttu-id="f9910-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f9910-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9910-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f9910-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f9910-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9910-133">See also</span></span>

- [<span data-ttu-id="f9910-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f9910-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

