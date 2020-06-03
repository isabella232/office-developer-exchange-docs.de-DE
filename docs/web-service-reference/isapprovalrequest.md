---
title: IsApprovalRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsApprovalRequest
api_type:
- schema
ms.assetid: 293ed01b-f6a4-4459-819c-933bbfaa2dd7
description: Das IsApprovalRequest-Element gibt an, ob eingehende Nachrichten Genehmigungsanforderungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 08ea36820b2680bb2c7e5695eb2dd481154c05eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530016"
---
# <a name="isapprovalrequest"></a><span data-ttu-id="7b957-103">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="7b957-103">IsApprovalRequest</span></span>

<span data-ttu-id="7b957-104">Das **IsApprovalRequest** -Element gibt an, ob eingehende Nachrichten Genehmigungsanforderungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="7b957-104">The **IsApprovalRequest** element indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span> 
  
```XML
<IsApprovalRequest/>
```

 <span data-ttu-id="7b957-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7b957-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b957-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7b957-106">Attributes and elements</span></span>

<span data-ttu-id="7b957-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b957-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b957-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7b957-108">Attributes</span></span>

<span data-ttu-id="7b957-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b957-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b957-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b957-110">Child elements</span></span>

<span data-ttu-id="7b957-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b957-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7b957-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b957-112">Parent elements</span></span>

|<span data-ttu-id="7b957-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b957-113">**Element**</span></span>|<span data-ttu-id="7b957-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b957-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b957-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="7b957-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7b957-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="7b957-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7b957-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="7b957-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7b957-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="7b957-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7b957-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="7b957-119">Text value</span></span>

<span data-ttu-id="7b957-120">Der Textwert **true** gibt an, dass die Nachricht eine Genehmigungsanforderung sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="7b957-120">A text value of **true** indicates that the message must be an approval request in order for the condition or exception to apply.</span></span> <span data-ttu-id="7b957-121">Der Wert **false** gibt an, dass die Nachricht keine Genehmigungsanforderung sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="7b957-121">A value of **false** indicates that the message must not be an approval request in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b957-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b957-122">Remarks</span></span>

<span data-ttu-id="7b957-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7b957-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b957-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7b957-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b957-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b957-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b957-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7b957-126">Schema Name</span></span>  <br/> |<span data-ttu-id="7b957-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7b957-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b957-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7b957-128">Validation File</span></span>  <br/> |<span data-ttu-id="7b957-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7b957-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b957-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7b957-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b957-131">True</span><span class="sxs-lookup"><span data-stu-id="7b957-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b957-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b957-132">See also</span></span>



- [<span data-ttu-id="7b957-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7b957-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

