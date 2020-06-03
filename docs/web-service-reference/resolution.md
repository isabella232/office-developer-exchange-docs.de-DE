---
title: Lösung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resolution
api_type:
- schema
ms.assetid: 573bed4b-d7b1-4baf-b16f-0795cdebf1a7
description: Das Auflösungs Element enthält eine einzelne aufgelöste Entität.
ms.openlocfilehash: 63c80f3c8d7dabf7e6dc1494df04c0be821b28bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468285"
---
# <a name="resolution"></a><span data-ttu-id="59ae1-103">Lösung</span><span class="sxs-lookup"><span data-stu-id="59ae1-103">Resolution</span></span>

<span data-ttu-id="59ae1-104">Das **Auflösungs** Element enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="59ae1-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="59ae1-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="59ae1-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="59ae1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59ae1-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="59ae1-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59ae1-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="59ae1-108">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="59ae1-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="59ae1-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="59ae1-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="59ae1-110">**Resolutiontype**</span><span class="sxs-lookup"><span data-stu-id="59ae1-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59ae1-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="59ae1-111">Attributes and elements</span></span>

<span data-ttu-id="59ae1-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="59ae1-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59ae1-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="59ae1-113">Attributes</span></span>

<span data-ttu-id="59ae1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="59ae1-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59ae1-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59ae1-115">Child elements</span></span>

|<span data-ttu-id="59ae1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="59ae1-116">**Element**</span></span>|<span data-ttu-id="59ae1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59ae1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59ae1-118">Postfach</span><span class="sxs-lookup"><span data-stu-id="59ae1-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="59ae1-119">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="59ae1-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="59ae1-120">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="59ae1-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="59ae1-121">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="59ae1-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59ae1-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59ae1-122">Parent elements</span></span>

|<span data-ttu-id="59ae1-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="59ae1-123">**Element**</span></span>|<span data-ttu-id="59ae1-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59ae1-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59ae1-125">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="59ae1-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="59ae1-126">Enthält ein Array von Auflösungen für einen eindeutigen Namen.</span><span class="sxs-lookup"><span data-stu-id="59ae1-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59ae1-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59ae1-127">Remarks</span></span>

<span data-ttu-id="59ae1-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="59ae1-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59ae1-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="59ae1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59ae1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="59ae1-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59ae1-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="59ae1-131">Schema name</span></span>  <br/> |<span data-ttu-id="59ae1-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="59ae1-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="59ae1-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="59ae1-133">Validation file</span></span>  <br/> |<span data-ttu-id="59ae1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="59ae1-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59ae1-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="59ae1-135">Can be empty</span></span>  <br/> |<span data-ttu-id="59ae1-136">False</span><span class="sxs-lookup"><span data-stu-id="59ae1-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59ae1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59ae1-137">See also</span></span>



[<span data-ttu-id="59ae1-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="59ae1-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="59ae1-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="59ae1-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="59ae1-140">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="59ae1-140">ResolveNames operation</span></span>](resolvenames-operation.md)

