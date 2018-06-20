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
description: Das IsNDR-Element gibt an, ob eingehende Nachrichten Unzustellbarkeitsberichte (NDR) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.
ms.openlocfilehash: 651590d055a0532c904dbf6c481dca2f899d673f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830056"
---
# <a name="isndr"></a><span data-ttu-id="b1b08-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="b1b08-103">IsNDR</span></span>

<span data-ttu-id="b1b08-104">Das **IsNDR** -Element gibt an, ob eingehende Nachrichten Unzustellbarkeitsberichte (NDR) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="b1b08-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="b1b08-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b1b08-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1b08-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b1b08-106">Attributes and elements</span></span>

<span data-ttu-id="b1b08-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b1b08-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1b08-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b1b08-108">Attributes</span></span>

<span data-ttu-id="b1b08-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1b08-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1b08-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1b08-110">Child elements</span></span>

<span data-ttu-id="b1b08-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1b08-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1b08-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1b08-112">Parent elements</span></span>

|<span data-ttu-id="b1b08-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1b08-113">**Element**</span></span>|<span data-ttu-id="b1b08-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1b08-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1b08-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="b1b08-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b1b08-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="b1b08-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b1b08-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="b1b08-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b1b08-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="b1b08-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1b08-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b1b08-119">Text value</span></span>

<span data-ttu-id="b1b08-120">Der Textwert **true** gibt an, dass die Nachricht eines Unzustellbarkeitsberichts in Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="b1b08-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="b1b08-121">Der Wert **false** gibt an, dass die Nachricht keines Unzustellbarkeitsberichts in Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="b1b08-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b1b08-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1b08-122">Remarks</span></span>

<span data-ttu-id="b1b08-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b1b08-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1b08-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b1b08-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1b08-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1b08-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1b08-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b1b08-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b1b08-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b1b08-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1b08-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b1b08-128">Validation File</span></span>  <br/> |<span data-ttu-id="b1b08-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1b08-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1b08-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b1b08-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1b08-131">True</span><span class="sxs-lookup"><span data-stu-id="b1b08-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1b08-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1b08-132">See also</span></span>



- [<span data-ttu-id="b1b08-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b1b08-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

