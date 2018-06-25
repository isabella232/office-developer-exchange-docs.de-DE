---
title: ApprovalRequestData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6c971cf7-5c3a-4e5e-9a7d-048f4ac0aadb
description: Das ApprovalRequestData-Element gibt den Status Genehmigung eine Genehmigung Request-Nachricht.
ms.openlocfilehash: ed1c1e3db4edd2cf4de032dc61abd73e863d4f1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757367"
---
# <a name="approvalrequestdata"></a><span data-ttu-id="c0f96-103">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="c0f96-103">ApprovalRequestData</span></span>

<span data-ttu-id="c0f96-104">Das **ApprovalRequestData** -Element gibt den Status Genehmigung eine Genehmigung Request-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c0f96-104">The **ApprovalRequestData** element specifies the approval state of an approval request message.</span></span> 
  
```xml
<ApprovalRequestData>
   <IsUndecidedApprovalRequest/>
   <ApprovalDecision/>
   <ApprovalDecisionMaker/>
   <ApprovalDecisionTime/>
</ApprovalRequestData>
```

 <span data-ttu-id="c0f96-105">**ApprovalRequestDataType**</span><span class="sxs-lookup"><span data-stu-id="c0f96-105">**ApprovalRequestDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0f96-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0f96-106">Attributes and elements</span></span>

<span data-ttu-id="c0f96-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0f96-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0f96-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0f96-108">Attributes</span></span>

<span data-ttu-id="c0f96-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0f96-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0f96-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0f96-110">Child elements</span></span>

<span data-ttu-id="c0f96-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span><span class="sxs-lookup"><span data-stu-id="c0f96-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0f96-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0f96-112">Parent elements</span></span>

[<span data-ttu-id="c0f96-113">Message</span><span class="sxs-lookup"><span data-stu-id="c0f96-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="c0f96-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0f96-114">Remarks</span></span>

<span data-ttu-id="c0f96-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c0f96-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="c0f96-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c0f96-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0f96-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0f96-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0f96-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0f96-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0f96-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0f96-119">Schema Name</span></span>  <br/> |<span data-ttu-id="c0f96-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c0f96-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0f96-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0f96-121">Validation File</span></span>  <br/> |<span data-ttu-id="c0f96-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0f96-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0f96-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0f96-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0f96-124">True</span><span class="sxs-lookup"><span data-stu-id="c0f96-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0f96-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0f96-125">See also</span></span>

- [<span data-ttu-id="c0f96-126">Message</span><span class="sxs-lookup"><span data-stu-id="c0f96-126">Message</span></span>](message-ex15websvcsotherref.md)
- [<span data-ttu-id="c0f96-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c0f96-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

