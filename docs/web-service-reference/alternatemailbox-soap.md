---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: Das AlternateMailbox-Element stellt ein alternative-Postfach.
ms.openlocfilehash: 8eb53e4846ad55916e2c5876606c00c0f2e371ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757309"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="0da90-103">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="0da90-104">Das **AlternateMailbox** -Element stellt ein alternative-Postfach.</span><span class="sxs-lookup"><span data-stu-id="0da90-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="0da90-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="0da90-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0da90-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0da90-106">Attributes and elements</span></span>

<span data-ttu-id="0da90-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0da90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0da90-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0da90-108">Attributes</span></span>

<span data-ttu-id="0da90-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0da90-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0da90-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0da90-110">Child elements</span></span>

|<span data-ttu-id="0da90-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0da90-111">**Element**</span></span>|<span data-ttu-id="0da90-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0da90-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0da90-113">Typ (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="0da90-114">Stellt die alternative Postfachtyp.</span><span class="sxs-lookup"><span data-stu-id="0da90-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="0da90-115">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="0da90-116">Stellt den Anzeigenamen alternative Postfach an.</span><span class="sxs-lookup"><span data-stu-id="0da90-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="0da90-117">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="0da90-118">Alternative Postfach legacy-DN darstellt.</span><span class="sxs-lookup"><span data-stu-id="0da90-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="0da90-119">Server (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="0da90-120">Stellt den alternative Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="0da90-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="0da90-121">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="0da90-122">Stellt das alternative Postfach SMTP-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="0da90-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0da90-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0da90-123">Parent elements</span></span>

|<span data-ttu-id="0da90-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0da90-124">**Element**</span></span>|<span data-ttu-id="0da90-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0da90-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0da90-126">AlternateMailboxes (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="0da90-127">Stellt eine Auflistung von alternativen Postfächern.</span><span class="sxs-lookup"><span data-stu-id="0da90-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0da90-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="0da90-128">Text value</span></span>

<span data-ttu-id="0da90-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="0da90-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0da90-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0da90-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0da90-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0da90-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0da90-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0da90-132">Schema Name</span></span>  <br/> |<span data-ttu-id="0da90-133">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="0da90-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0da90-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0da90-134">Validation File</span></span>  <br/> |<span data-ttu-id="0da90-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0da90-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0da90-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0da90-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="0da90-137">True</span><span class="sxs-lookup"><span data-stu-id="0da90-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0da90-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0da90-138">See also</span></span>

- [<span data-ttu-id="0da90-139">AlternateMailboxCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0da90-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)

