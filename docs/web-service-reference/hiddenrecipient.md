---
title: HiddenRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HiddenRecipient
api_type:
- schema
ms.assetid: a8209f75-0070-4424-8dcd-273cfd192728
description: Das HiddenRecipient-Element gibt an, dass der Empfänger von einer Organisationsrichtlinie hinzugefügt wurde, die von unprivilegierten Benutzern ausgeblendet werden sollte.
ms.openlocfilehash: bfe57fabc02ff00c801672b71ccdb0bf1b916bd9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457641"
---
# <a name="hiddenrecipient"></a><span data-ttu-id="10995-103">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="10995-103">HiddenRecipient</span></span>

<span data-ttu-id="10995-104">Das **HiddenRecipient** -Element gibt an, dass der Empfänger von einer Organisationsrichtlinie hinzugefügt wurde, die von unprivilegierten Benutzern ausgeblendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="10995-104">The **HiddenRecipient** element indicates that the recipient was added by an organization policy that should be hidden from unprivileged users.</span></span> 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
```

 <span data-ttu-id="10995-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="10995-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10995-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="10995-106">Attributes and elements</span></span>

<span data-ttu-id="10995-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="10995-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10995-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="10995-108">Attributes</span></span>

<span data-ttu-id="10995-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="10995-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10995-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10995-110">Child elements</span></span>

<span data-ttu-id="10995-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="10995-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10995-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10995-112">Parent elements</span></span>

|<span data-ttu-id="10995-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="10995-113">**Element**</span></span>|<span data-ttu-id="10995-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10995-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10995-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="10995-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="10995-116">Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="10995-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10995-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="10995-117">Text value</span></span>

<span data-ttu-id="10995-118">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="10995-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="10995-119">Der Wert **true** gibt an, dass der Benutzer von einer Organisationsrichtlinie hinzugefügt wurde; der Wert **false** gibt an, dass der Benutzer nicht von einer Organisationsrichtlinie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="10995-119">A value of **true** indicates that the user was added by an organization policy; a value of **false** indicates that the user was not added by an organization policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10995-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10995-120">Remarks</span></span>

<span data-ttu-id="10995-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="10995-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10995-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="10995-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10995-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="10995-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10995-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="10995-124">Schema Name</span></span>  <br/> |<span data-ttu-id="10995-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="10995-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="10995-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="10995-126">Validation File</span></span>  <br/> |<span data-ttu-id="10995-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="10995-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10995-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="10995-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="10995-129">False</span><span class="sxs-lookup"><span data-stu-id="10995-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10995-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10995-130">See also</span></span>



- [<span data-ttu-id="10995-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="10995-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

