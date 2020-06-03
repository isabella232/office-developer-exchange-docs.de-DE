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
description: Das AlternateMailbox-Element stellt ein alternatives Postfach dar.
ms.openlocfilehash: 9019f85a373cc186cc9dadddceee3dc9d11b3854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466157"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="c3f01-103">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="c3f01-104">Das **AlternateMailbox** -Element stellt ein alternatives Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="c3f01-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="c3f01-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3f01-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c3f01-106">Attributes and elements</span></span>

<span data-ttu-id="c3f01-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c3f01-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3f01-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c3f01-108">Attributes</span></span>

<span data-ttu-id="c3f01-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3f01-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3f01-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3f01-110">Child elements</span></span>

|<span data-ttu-id="c3f01-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3f01-111">**Element**</span></span>|<span data-ttu-id="c3f01-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3f01-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3f01-113">Type (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="c3f01-114">Stellt den alternativen Postfachtyp dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="c3f01-115">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="c3f01-116">Stellt den Anzeigenamen des alternativen Postfachs dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="c3f01-117">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="c3f01-118">Stellt den Distinguished Name des alternativen Post Fach Legacy dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="c3f01-119">Server (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="c3f01-120">Stellt den alternativen Postfachserver dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="c3f01-121">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="c3f01-122">Stellt die Alternative Post Fach SMTP-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c3f01-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3f01-123">Parent elements</span></span>

|<span data-ttu-id="c3f01-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3f01-124">**Element**</span></span>|<span data-ttu-id="c3f01-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3f01-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3f01-126">AlternateMailboxes (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="c3f01-127">Stellt eine Auflistung von alternativen Postfächern dar.</span><span class="sxs-lookup"><span data-stu-id="c3f01-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c3f01-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="c3f01-128">Text value</span></span>

<span data-ttu-id="c3f01-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3f01-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3f01-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c3f01-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3f01-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3f01-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c3f01-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c3f01-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c3f01-133">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="c3f01-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c3f01-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c3f01-134">Validation File</span></span>  <br/> |<span data-ttu-id="c3f01-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c3f01-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c3f01-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c3f01-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c3f01-137">True</span><span class="sxs-lookup"><span data-stu-id="c3f01-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3f01-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f01-138">See also</span></span>

- [<span data-ttu-id="c3f01-139">AlternateMailboxCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3f01-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)

