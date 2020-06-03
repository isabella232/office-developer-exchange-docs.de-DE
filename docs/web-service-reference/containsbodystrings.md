---
title: ContainsBodyStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsBodyStrings
api_type:
- schema
ms.assetid: 70639472-64bb-456a-8b40-dce727542443
description: Das ContainsBodyStrings-Element gibt die Zeichenfolgen an, die im Textkörper von eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 008261ab94b1bed33cc72cacf7abe7aa58927d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463804"
---
# <a name="containsbodystrings"></a><span data-ttu-id="49723-103">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="49723-103">ContainsBodyStrings</span></span>

<span data-ttu-id="49723-104">Das **ContainsBodyStrings** -Element gibt die Zeichenfolgen an, die im Textkörper von eingehenden Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="49723-104">The **ContainsBodyStrings** element indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsBodyStrings>
    <String/>
</ContainsBodyStrings>
```

 <span data-ttu-id="49723-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="49723-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49723-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="49723-106">Attributes and elements</span></span>

<span data-ttu-id="49723-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="49723-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49723-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="49723-108">Attributes</span></span>

<span data-ttu-id="49723-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="49723-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49723-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49723-110">Child elements</span></span>

|<span data-ttu-id="49723-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="49723-111">**Element**</span></span>|<span data-ttu-id="49723-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49723-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49723-113">String</span><span class="sxs-lookup"><span data-stu-id="49723-113">String</span></span>](string.md) <br/> |<span data-ttu-id="49723-114">Stellt eine Zeichenfolge dar, die im Textkörper von eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="49723-114">Represents a string that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="49723-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49723-115">Parent elements</span></span>

|<span data-ttu-id="49723-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="49723-116">**Element**</span></span>|<span data-ttu-id="49723-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49723-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49723-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="49723-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="49723-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="49723-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="49723-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="49723-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="49723-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="49723-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49723-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="49723-122">Text value</span></span>

<span data-ttu-id="49723-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="49723-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49723-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49723-124">Remarks</span></span>

<span data-ttu-id="49723-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="49723-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49723-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="49723-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49723-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="49723-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="49723-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="49723-128">Schema Name</span></span>  <br/> |<span data-ttu-id="49723-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="49723-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="49723-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="49723-130">Validation File</span></span>  <br/> |<span data-ttu-id="49723-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="49723-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="49723-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="49723-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="49723-133">True</span><span class="sxs-lookup"><span data-stu-id="49723-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49723-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49723-134">See also</span></span>



- [<span data-ttu-id="49723-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="49723-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

