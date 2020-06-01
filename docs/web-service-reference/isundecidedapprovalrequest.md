---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: Das IsUndecidedApprovalRequest-Element gibt an, ob eine Genehmigungs Anforderungsnachricht verarbeitet wurde.
ms.openlocfilehash: 0949cf64b8583c4b3fa5a1700475f01cc480f69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458173"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="ac48f-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="ac48f-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="ac48f-104">Das **IsUndecidedApprovalRequest** -Element gibt an, ob eine Genehmigungs Anforderungsnachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac48f-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="ac48f-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ac48f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac48f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac48f-106">Attributes and elements</span></span>

<span data-ttu-id="ac48f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac48f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac48f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac48f-108">Attributes</span></span>

<span data-ttu-id="ac48f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac48f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac48f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac48f-110">Child elements</span></span>

<span data-ttu-id="ac48f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac48f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac48f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac48f-112">Parent elements</span></span>

[<span data-ttu-id="ac48f-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="ac48f-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="ac48f-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ac48f-114">Text value</span></span>

<span data-ttu-id="ac48f-115">Der Textwert des **IsUndecidedApprovalRequest** -Elements ist **true** , wenn keine Genehmigungs Anforderungsnachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ac48f-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="ac48f-116">Der Wert **false** gibt an, dass die Genehmigungsanforderung entschieden wurde.</span><span class="sxs-lookup"><span data-stu-id="ac48f-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ac48f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac48f-117">Remarks</span></span>

<span data-ttu-id="ac48f-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ac48f-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="ac48f-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ac48f-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac48f-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac48f-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac48f-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac48f-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac48f-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac48f-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ac48f-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ac48f-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac48f-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac48f-124">Validation File</span></span>  <br/> |<span data-ttu-id="ac48f-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac48f-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac48f-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac48f-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac48f-127">True</span><span class="sxs-lookup"><span data-stu-id="ac48f-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac48f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac48f-128">See also</span></span>



[<span data-ttu-id="ac48f-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="ac48f-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="ac48f-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac48f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

