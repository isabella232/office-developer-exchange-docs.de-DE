---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: Das OutlookRuleBlobExists-Element gibt an, ob ein Microsoft Outlook-Regel Blob im Postfach des Benutzers vorhanden ist.
ms.openlocfilehash: a738377cd3c1d69b90ac39ca479b03b3220d5bc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830679"
---
# <a name="outlookruleblobexists"></a><span data-ttu-id="530fb-103">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="530fb-103">OutlookRuleBlobExists</span></span>

<span data-ttu-id="530fb-104">Das **OutlookRuleBlobExists** -Element gibt an, ob ein Microsoft Outlook-Regel Blob im Postfach des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="530fb-104">The **OutlookRuleBlobExists** element indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span> 
  
[<span data-ttu-id="530fb-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="530fb-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="530fb-106">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="530fb-106">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 <span data-ttu-id="530fb-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="530fb-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="530fb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="530fb-108">Attributes and elements</span></span>

<span data-ttu-id="530fb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="530fb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="530fb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="530fb-110">Attributes</span></span>

<span data-ttu-id="530fb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="530fb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="530fb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="530fb-112">Child elements</span></span>

<span data-ttu-id="530fb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="530fb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="530fb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="530fb-114">Parent elements</span></span>

|<span data-ttu-id="530fb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="530fb-115">**Element**</span></span>|<span data-ttu-id="530fb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="530fb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="530fb-117">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="530fb-117">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="530fb-118">Stellt eine Antwort auf eine Anforderung [GetInboxRules Vorgang](getinboxrules-operation.md) dar.</span><span class="sxs-lookup"><span data-stu-id="530fb-118">Represents a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="530fb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="530fb-119">Text value</span></span>

<span data-ttu-id="530fb-120">Der Textwert **true** gibt an, dass ein Outlook-Regel Blob vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="530fb-120">A text value of **true** indicates that an Outlook rule blob exists.</span></span> <span data-ttu-id="530fb-121">Der Textwert **false** gibt an, dass ein Outlook-Regel Blob nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="530fb-121">A text value of **false** indicates that an Outlook rule blob does not exist.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="530fb-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="530fb-122">Remarks</span></span>

<span data-ttu-id="530fb-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="530fb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="530fb-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="530fb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="530fb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="530fb-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="530fb-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="530fb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="530fb-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="530fb-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="530fb-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="530fb-128">Validation File</span></span>  <br/> |<span data-ttu-id="530fb-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="530fb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="530fb-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="530fb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="530fb-131">True</span><span class="sxs-lookup"><span data-stu-id="530fb-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="530fb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="530fb-132">See also</span></span>



- [<span data-ttu-id="530fb-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="530fb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

