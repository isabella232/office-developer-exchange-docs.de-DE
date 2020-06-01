---
title: ContainsSenderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSenderStrings
api_type:
- schema
ms.assetid: 3e16163f-cffe-4c4e-9a2a-00245d25ba96
description: Das ContainsSenderStrings-Element gibt die Zeichenfolgen an, die in der From-Eigenschaft eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: e7b78f1311d288db7969a0024bde84433e18d37f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458978"
---
# <a name="containssenderstrings"></a><span data-ttu-id="546aa-103">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="546aa-103">ContainsSenderStrings</span></span>

<span data-ttu-id="546aa-104">Das **ContainsSenderStrings** -Element gibt die Zeichenfolgen an, die in der **from** -Eigenschaft eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="546aa-104">The **ContainsSenderStrings** element indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSenderStrings>
    <String/>
</ContainsSenderStrings>
```

 <span data-ttu-id="546aa-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="546aa-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="546aa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="546aa-106">Attributes and elements</span></span>

<span data-ttu-id="546aa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="546aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="546aa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="546aa-108">Attributes</span></span>

<span data-ttu-id="546aa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="546aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="546aa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546aa-110">Child elements</span></span>

|<span data-ttu-id="546aa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="546aa-111">**Element**</span></span>|<span data-ttu-id="546aa-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546aa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="546aa-113">String</span><span class="sxs-lookup"><span data-stu-id="546aa-113">String</span></span>](string.md) <br/> |<span data-ttu-id="546aa-114">Stellt eine Zeichenfolge dar, die in der **from** -Eigenschaft eingehender Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="546aa-114">Represents a string that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="546aa-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546aa-115">Parent elements</span></span>

|<span data-ttu-id="546aa-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="546aa-116">**Element**</span></span>|<span data-ttu-id="546aa-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546aa-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="546aa-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="546aa-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="546aa-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="546aa-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="546aa-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="546aa-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="546aa-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="546aa-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="546aa-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="546aa-122">Text value</span></span>

<span data-ttu-id="546aa-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="546aa-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="546aa-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="546aa-124">Remarks</span></span>

<span data-ttu-id="546aa-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="546aa-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="546aa-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="546aa-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="546aa-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="546aa-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="546aa-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="546aa-128">Schema Name</span></span>  <br/> |<span data-ttu-id="546aa-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="546aa-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="546aa-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="546aa-130">Validation File</span></span>  <br/> |<span data-ttu-id="546aa-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="546aa-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="546aa-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="546aa-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="546aa-133">True</span><span class="sxs-lookup"><span data-stu-id="546aa-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="546aa-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="546aa-134">See also</span></span>



- [<span data-ttu-id="546aa-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="546aa-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

