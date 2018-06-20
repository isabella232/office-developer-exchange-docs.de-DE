---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: Das IsUndecidedApprovalRequest-Element gibt an, ob eine Genehmigung Request-Nachricht auf gefasst.
ms.openlocfilehash: 82b4624df5b2fe7ca212fdf76248e1ccfa3a081f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830127"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="24ea2-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="24ea2-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="24ea2-104">Das **IsUndecidedApprovalRequest** -Element gibt an, ob eine Genehmigung Request-Nachricht auf gefasst.</span><span class="sxs-lookup"><span data-stu-id="24ea2-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="24ea2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="24ea2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24ea2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24ea2-106">Attributes and elements</span></span>

<span data-ttu-id="24ea2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24ea2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24ea2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="24ea2-108">Attributes</span></span>

<span data-ttu-id="24ea2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="24ea2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24ea2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24ea2-110">Child elements</span></span>

<span data-ttu-id="24ea2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="24ea2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24ea2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24ea2-112">Parent elements</span></span>

[<span data-ttu-id="24ea2-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="24ea2-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="24ea2-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="24ea2-114">Text value</span></span>

<span data-ttu-id="24ea2-115">Der Textwert der **IsUndecidedApprovalRequest** -Element ist **true** , wenn eine Genehmigung Request-Nachricht nicht auf tätig geworden ist.</span><span class="sxs-lookup"><span data-stu-id="24ea2-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="24ea2-116">Der Wert **false** gibt an, dass die genehmigungsanforderung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="24ea2-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24ea2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24ea2-117">Remarks</span></span>

<span data-ttu-id="24ea2-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="24ea2-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="24ea2-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="24ea2-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24ea2-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="24ea2-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24ea2-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="24ea2-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24ea2-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24ea2-122">Schema Name</span></span>  <br/> |<span data-ttu-id="24ea2-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="24ea2-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="24ea2-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24ea2-124">Validation File</span></span>  <br/> |<span data-ttu-id="24ea2-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24ea2-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24ea2-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="24ea2-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="24ea2-127">True</span><span class="sxs-lookup"><span data-stu-id="24ea2-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24ea2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24ea2-128">See also</span></span>



[<span data-ttu-id="24ea2-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="24ea2-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="24ea2-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="24ea2-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

