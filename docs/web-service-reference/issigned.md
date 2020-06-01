---
title: IsSigned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsSigned
api_type:
- schema
ms.assetid: a4f90fe5-2834-4621-9aa3-b561f74d4674
description: Das IsSigned-Element gibt an, ob eingehende Nachrichten signiert werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: fe8551d01e6f9e813da8936f15b0b7ba1d4ce56c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455527"
---
# <a name="issigned"></a><span data-ttu-id="4aacb-103">IsSigned</span><span class="sxs-lookup"><span data-stu-id="4aacb-103">IsSigned</span></span>

<span data-ttu-id="4aacb-104">Das **IsSigned** -Element gibt an, ob eingehende Nachrichten signiert werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4aacb-104">The **IsSigned** element indicates whether incoming messages must be signed in order for the condition or exception to apply.</span></span> 
  
```XML
<IsSigned>true | false</IsSigned>
```

 <span data-ttu-id="4aacb-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="4aacb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4aacb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4aacb-106">Attributes and elements</span></span>

<span data-ttu-id="4aacb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4aacb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4aacb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4aacb-108">Attributes</span></span>

<span data-ttu-id="4aacb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4aacb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4aacb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4aacb-110">Child elements</span></span>

<span data-ttu-id="4aacb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4aacb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4aacb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4aacb-112">Parent elements</span></span>

|<span data-ttu-id="4aacb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4aacb-113">**Element**</span></span>|<span data-ttu-id="4aacb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4aacb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4aacb-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="4aacb-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="4aacb-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4aacb-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="4aacb-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="4aacb-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="4aacb-118">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="4aacb-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4aacb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="4aacb-119">Text value</span></span>

<span data-ttu-id="4aacb-120">Der Textwert **true** gibt an, dass die Nachricht signiert werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4aacb-120">A text value of **true** indicates that the message must be signed in order for the condition or exception to apply.</span></span> <span data-ttu-id="4aacb-121">Der Textwert **false** gibt an, dass die Nachricht nicht für die Bedingung oder Ausnahme signiert werden muss, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4aacb-121">A text value of **false** indicates that the message does not have to be signed for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4aacb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aacb-122">Remarks</span></span>

<span data-ttu-id="4aacb-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4aacb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4aacb-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4aacb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4aacb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4aacb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4aacb-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4aacb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4aacb-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4aacb-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4aacb-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4aacb-128">Validation File</span></span>  <br/> |<span data-ttu-id="4aacb-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4aacb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4aacb-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4aacb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4aacb-131">True</span><span class="sxs-lookup"><span data-stu-id="4aacb-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4aacb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aacb-132">See also</span></span>



- [<span data-ttu-id="4aacb-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4aacb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

