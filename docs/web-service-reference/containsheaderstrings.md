---
title: ContainsHeaderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsHeaderStrings
api_type:
- schema
ms.assetid: 5f68427b-990a-4a27-bfb3-fce3115b02d7
description: Das ContainsHeaderStrings-Element gibt die Zeichenfolgen an, die in den Kopfzeilen eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 23e3d0e7cff9c78edbac10a6275514af93cab325
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458992"
---
# <a name="containsheaderstrings"></a><span data-ttu-id="dd07a-103">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="dd07a-103">ContainsHeaderStrings</span></span>

<span data-ttu-id="dd07a-104">Das **ContainsHeaderStrings** -Element gibt die Zeichenfolgen an, die in den Kopfzeilen eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="dd07a-104">The **ContainsHeaderStrings** element indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsHeaderStrings>
    <String/>
</ContainsHeaderStrings>
```

 <span data-ttu-id="dd07a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="dd07a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd07a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd07a-106">Attributes and elements</span></span>

<span data-ttu-id="dd07a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dd07a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd07a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd07a-108">Attributes</span></span>

<span data-ttu-id="dd07a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd07a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd07a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd07a-110">Child elements</span></span>

|<span data-ttu-id="dd07a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd07a-111">**Element**</span></span>|<span data-ttu-id="dd07a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd07a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd07a-113">String</span><span class="sxs-lookup"><span data-stu-id="dd07a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="dd07a-114">Stellt eine Zeichenfolge dar, die in Nachrichtenkopfzeilen angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="dd07a-114">Represents a string that must appear in message headers in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd07a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd07a-115">Parent elements</span></span>

|<span data-ttu-id="dd07a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd07a-116">**Element**</span></span>|<span data-ttu-id="dd07a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd07a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd07a-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="dd07a-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="dd07a-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="dd07a-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="dd07a-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="dd07a-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="dd07a-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="dd07a-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd07a-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="dd07a-122">Text value</span></span>

<span data-ttu-id="dd07a-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd07a-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd07a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd07a-124">Remarks</span></span>

<span data-ttu-id="dd07a-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dd07a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd07a-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dd07a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd07a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd07a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd07a-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd07a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="dd07a-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dd07a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd07a-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd07a-130">Validation File</span></span>  <br/> |<span data-ttu-id="dd07a-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dd07a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd07a-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dd07a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd07a-133">True</span><span class="sxs-lookup"><span data-stu-id="dd07a-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd07a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd07a-134">See also</span></span>



- [<span data-ttu-id="dd07a-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dd07a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

