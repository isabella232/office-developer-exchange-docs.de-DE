---
title: IsNDR
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNDR
api_type:
- schema
ms.assetid: 194f5836-7793-463a-a090-4386d1c2487a
description: Das IsNDR-Element gibt an, ob eingehende Nachrichten nicht Zustellungsberichte (NDR) sein müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 3476331ccece347686b7f98edf49df5d48b8562e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458159"
---
# <a name="isndr"></a><span data-ttu-id="4960d-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="4960d-103">IsNDR</span></span>

<span data-ttu-id="4960d-104">Das **IsNDR** -Element gibt an, ob eingehende Nachrichten nicht Zustellungsberichte (NDR) sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4960d-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="4960d-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="4960d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4960d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4960d-106">Attributes and elements</span></span>

<span data-ttu-id="4960d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4960d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4960d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4960d-108">Attributes</span></span>

<span data-ttu-id="4960d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4960d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4960d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4960d-110">Child elements</span></span>

<span data-ttu-id="4960d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4960d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4960d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4960d-112">Parent elements</span></span>

|<span data-ttu-id="4960d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4960d-113">**Element**</span></span>|<span data-ttu-id="4960d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4960d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4960d-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="4960d-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="4960d-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4960d-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="4960d-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="4960d-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="4960d-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="4960d-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4960d-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="4960d-119">Text value</span></span>

<span data-ttu-id="4960d-120">Der Textwert **true** gibt an, dass die Nachricht ein Unzustellbarkeitsbericht sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4960d-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="4960d-121">Der Wert **false** gibt an, dass die Nachricht kein Unzustellbarkeitsbericht sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4960d-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4960d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4960d-122">Remarks</span></span>

<span data-ttu-id="4960d-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4960d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4960d-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4960d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4960d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4960d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4960d-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4960d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4960d-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4960d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4960d-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4960d-128">Validation File</span></span>  <br/> |<span data-ttu-id="4960d-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4960d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4960d-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4960d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4960d-131">True</span><span class="sxs-lookup"><span data-stu-id="4960d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4960d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4960d-132">See also</span></span>



- [<span data-ttu-id="4960d-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4960d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

