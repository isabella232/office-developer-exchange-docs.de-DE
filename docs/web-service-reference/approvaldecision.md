---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: Das ApprovalDecision-Element gibt die Entscheidung getroffen auf eine Genehmigung Request-Nachricht.
ms.openlocfilehash: 4ca73813440200e5d2fb9f920d81459d8cd5e4ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757363"
---
# <a name="approvaldecision"></a><span data-ttu-id="91a4c-103">ApprovalDecision</span><span class="sxs-lookup"><span data-stu-id="91a4c-103">ApprovalDecision</span></span>

<span data-ttu-id="91a4c-104">Das **ApprovalDecision** -Element gibt die Entscheidung getroffen auf eine Genehmigung Request-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91a4c-104">The **ApprovalDecision** element specifies the decision made on an approval request message.</span></span> 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 <span data-ttu-id="91a4c-105">**int**</span><span class="sxs-lookup"><span data-stu-id="91a4c-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91a4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91a4c-106">Attributes and elements</span></span>

<span data-ttu-id="91a4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91a4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91a4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="91a4c-108">Attributes</span></span>

<span data-ttu-id="91a4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="91a4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91a4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91a4c-110">Child elements</span></span>

<span data-ttu-id="91a4c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="91a4c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91a4c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91a4c-112">Parent elements</span></span>

[<span data-ttu-id="91a4c-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="91a4c-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="91a4c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="91a4c-114">Text value</span></span>

<span data-ttu-id="91a4c-115">Der Textwert des **ApprovalDecision** -Elements ist, wenn genehmigt 1 und 2 wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="91a4c-115">The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="91a4c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91a4c-116">Remarks</span></span>

<span data-ttu-id="91a4c-117">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="91a4c-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="91a4c-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="91a4c-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91a4c-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="91a4c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91a4c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="91a4c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91a4c-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91a4c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="91a4c-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="91a4c-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="91a4c-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91a4c-123">Validation File</span></span>  <br/> |<span data-ttu-id="91a4c-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91a4c-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91a4c-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="91a4c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="91a4c-126">True</span><span class="sxs-lookup"><span data-stu-id="91a4c-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91a4c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91a4c-127">See also</span></span>

- [<span data-ttu-id="91a4c-128">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="91a4c-128">ApprovalRequestData</span></span>](approvalrequestdata.md)
- [<span data-ttu-id="91a4c-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="91a4c-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

