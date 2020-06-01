---
title: IsAutomaticForward
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticForward
api_type:
- schema
ms.assetid: 6876b849-a648-482e-8934-93eb5a0c465f
description: Das IsAutomaticForward-Element gibt an, ob eingehende Nachrichten automatisch weitergeleitet werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 800d38bab30245d88b3c09609e6235e6de8fed25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455576"
---
# <a name="isautomaticforward"></a><span data-ttu-id="cac83-103">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="cac83-103">IsAutomaticForward</span></span>

<span data-ttu-id="cac83-104">Das **IsAutomaticForward** -Element gibt an, ob eingehende Nachrichten automatisch weitergeleitet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="cac83-104">The **IsAutomaticForward** element indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticForward/> true | false</IsAutomaticForward>
```

 <span data-ttu-id="cac83-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="cac83-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cac83-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cac83-106">Attributes and elements</span></span>

<span data-ttu-id="cac83-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cac83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cac83-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cac83-108">Attributes</span></span>

<span data-ttu-id="cac83-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cac83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cac83-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cac83-110">Child elements</span></span>

<span data-ttu-id="cac83-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cac83-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cac83-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cac83-112">Parent elements</span></span>

|<span data-ttu-id="cac83-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cac83-113">**Element**</span></span>|<span data-ttu-id="cac83-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cac83-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cac83-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="cac83-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="cac83-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="cac83-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="cac83-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="cac83-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="cac83-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="cac83-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cac83-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="cac83-119">Text value</span></span>

<span data-ttu-id="cac83-120">Der Textwert **true** gibt an, dass die Nachricht automatisch weitergeleitet werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="cac83-120">A text value of **true** indicates that the message must be an automatic forward in order for the condition or exception to apply.</span></span> <span data-ttu-id="cac83-121">Der Wert **false** gibt an, dass die Nachricht nicht automatisch weitergeleitet werden darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="cac83-121">A value of **false** indicates that the message must not be an automatic forward in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cac83-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cac83-122">Remarks</span></span>

<span data-ttu-id="cac83-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cac83-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cac83-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cac83-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cac83-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="cac83-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cac83-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cac83-126">Schema Name</span></span>  <br/> |<span data-ttu-id="cac83-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cac83-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cac83-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cac83-128">Validation File</span></span>  <br/> |<span data-ttu-id="cac83-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cac83-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cac83-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cac83-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="cac83-131">True</span><span class="sxs-lookup"><span data-stu-id="cac83-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cac83-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac83-132">See also</span></span>



- [<span data-ttu-id="cac83-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cac83-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

