---
title: FindMailboxStatisticsByKeywordsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af1dd9bf-df47-473d-a2ce-ab9a01a37606
description: Das FindMailboxStatisticsByKeywordsResponse-Element gibt die Antwort auf eine FindMailboxStatisticsByKeywords-Anforderung an.
ms.openlocfilehash: a0595ec9ee0cedf5150852dc39eca50b598e15aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460988"
---
# <a name="findmailboxstatisticsbykeywordsresponse"></a><span data-ttu-id="4643f-103">FindMailboxStatisticsByKeywordsResponse</span><span class="sxs-lookup"><span data-stu-id="4643f-103">FindMailboxStatisticsByKeywordsResponse</span></span>

<span data-ttu-id="4643f-104">Das **FindMailboxStatisticsByKeywordsResponse** -Element gibt die Antwort auf eine **FindMailboxStatisticsByKeywords** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4643f-104">The **FindMailboxStatisticsByKeywordsResponse** element specifies the response to a **FindMailboxStatisticsByKeywords** request.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywordsResponse>
    <ResponseMessages/>
</FindMailboxStatisticsByKeywordsResponse>
```

 <span data-ttu-id="4643f-105">**FindMailboxStatisticsByKeywordsResponseType**</span><span class="sxs-lookup"><span data-stu-id="4643f-105">**FindMailboxStatisticsByKeywordsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4643f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4643f-106">Attributes and elements</span></span>

<span data-ttu-id="4643f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4643f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4643f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4643f-108">Attributes</span></span>

<span data-ttu-id="4643f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4643f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4643f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4643f-110">Child elements</span></span>

|<span data-ttu-id="4643f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4643f-111">**Element**</span></span>|<span data-ttu-id="4643f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4643f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4643f-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4643f-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4643f-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4643f-114">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4643f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4643f-115">Parent elements</span></span>

<span data-ttu-id="4643f-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4643f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4643f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4643f-117">Remarks</span></span>

<span data-ttu-id="4643f-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4643f-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4643f-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4643f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4643f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="4643f-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4643f-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4643f-121">Schema Name</span></span>  <br/> |<span data-ttu-id="4643f-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4643f-122">Message schema</span></span>  <br/> |
|<span data-ttu-id="4643f-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4643f-123">Validation File</span></span>  <br/> |<span data-ttu-id="4643f-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4643f-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4643f-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4643f-125">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4643f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4643f-126">See also</span></span>



- [<span data-ttu-id="4643f-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4643f-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

