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
description: Das IsPermissionControlled-Element gibt an, ob eingehende Nachrichten Berechtigung gesteuert (RMS geschützte) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.
ms.openlocfilehash: fdd9910b8c35d9d57e724d6fec57d203f38f0359
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830088"
---
# <a name="ispermissioncontrolled"></a><span data-ttu-id="4d6a4-103">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="4d6a4-103">IsPermissionControlled</span></span>

<span data-ttu-id="4d6a4-104">Das **IsPermissionControlled** -Element gibt an, ob eingehende Nachrichten Berechtigung gesteuert (RMS geschützte) müssen in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-104">The **IsPermissionControlled** element indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 <span data-ttu-id="4d6a4-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4d6a4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d6a4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4d6a4-106">Attributes and elements</span></span>

<span data-ttu-id="4d6a4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d6a4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4d6a4-108">Attributes</span></span>

<span data-ttu-id="4d6a4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d6a4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d6a4-110">Child elements</span></span>

<span data-ttu-id="4d6a4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d6a4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d6a4-112">Parent elements</span></span>

|<span data-ttu-id="4d6a4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d6a4-113">**Element**</span></span>|<span data-ttu-id="4d6a4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d6a4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d6a4-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="4d6a4-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="4d6a4-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="4d6a4-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="4d6a4-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="4d6a4-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4d6a4-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="4d6a4-119">Text value</span></span>

<span data-ttu-id="4d6a4-120">Der Textwert **true** gibt an, dass die Nachricht RMS in Reihenfolge für die Bedingung oder Ausnahme anzuwendende geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-120">A text value of **true** indicates that the message must be RMS protected in order for the condition or exception to apply.</span></span> <span data-ttu-id="4d6a4-121">Der Wert **false** gibt an, dass die Nachricht nicht RMS in Reihenfolge für die Bedingung oder Ausnahme anzuwendende geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-121">A value of **false** indicates that the message must not be RMS protected in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d6a4-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d6a4-122">Remarks</span></span>

<span data-ttu-id="4d6a4-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d6a4-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4d6a4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d6a4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d6a4-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d6a4-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4d6a4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4d6a4-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4d6a4-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4d6a4-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4d6a4-128">Validation File</span></span>  <br/> |<span data-ttu-id="4d6a4-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d6a4-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d6a4-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4d6a4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d6a4-131">True</span><span class="sxs-lookup"><span data-stu-id="4d6a4-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d6a4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d6a4-132">See also</span></span>



- [<span data-ttu-id="4d6a4-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d6a4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

