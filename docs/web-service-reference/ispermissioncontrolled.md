---
title: IsPermissionControlled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPermissionControlled
api_type:
- schema
ms.assetid: a2fd0340-f31f-4389-a1cd-7e93b40bb3c6
description: Das IsPermissionControlled-Element gibt an, ob eingehende Nachrichten berechtigungsgesteuert (RMS protected) sein müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 5fba06c1c56512f4a362f773f119ea346a4c0d2b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460386"
---
# <a name="ispermissioncontrolled"></a><span data-ttu-id="fe1e2-103">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="fe1e2-103">IsPermissionControlled</span></span>

<span data-ttu-id="fe1e2-104">Das **IsPermissionControlled** -Element gibt an, ob eingehende Nachrichten berechtigungsgesteuert (RMS protected) sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-104">The **IsPermissionControlled** element indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 <span data-ttu-id="fe1e2-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fe1e2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe1e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fe1e2-106">Attributes and elements</span></span>

<span data-ttu-id="fe1e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe1e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe1e2-108">Attributes</span></span>

<span data-ttu-id="fe1e2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe1e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe1e2-110">Child elements</span></span>

<span data-ttu-id="fe1e2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe1e2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe1e2-112">Parent elements</span></span>

|<span data-ttu-id="fe1e2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fe1e2-113">**Element**</span></span>|<span data-ttu-id="fe1e2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe1e2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe1e2-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="fe1e2-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="fe1e2-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="fe1e2-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="fe1e2-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="fe1e2-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe1e2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="fe1e2-119">Text value</span></span>

<span data-ttu-id="fe1e2-120">Der Textwert **true** gibt an, dass die Nachricht RMS-geschützt sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-120">A text value of **true** indicates that the message must be RMS protected in order for the condition or exception to apply.</span></span> <span data-ttu-id="fe1e2-121">Der Wert **false** gibt an, dass die Nachricht nicht RMS-geschützt sein darf, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-121">A value of **false** indicates that the message must not be RMS protected in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe1e2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe1e2-122">Remarks</span></span>

<span data-ttu-id="fe1e2-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fe1e2-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe1e2-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fe1e2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe1e2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe1e2-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe1e2-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fe1e2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fe1e2-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fe1e2-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe1e2-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fe1e2-128">Validation File</span></span>  <br/> |<span data-ttu-id="fe1e2-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fe1e2-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe1e2-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fe1e2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe1e2-131">True</span><span class="sxs-lookup"><span data-stu-id="fe1e2-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe1e2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe1e2-132">See also</span></span>



- [<span data-ttu-id="fe1e2-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fe1e2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

