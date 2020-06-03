---
title: ContainsSubjectOrBodyStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSubjectOrBodyStrings
api_type:
- schema
ms.assetid: 22aebf31-d9f4-4e03-bbff-c675409518d1
description: Das ContainsSubjectOrBodyStrings-Element gibt die Zeichenfolgen an, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 6f9c7862912632e7e86a0b704e760c7fd0f5f14c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466822"
---
# <a name="containssubjectorbodystrings"></a><span data-ttu-id="4f5f4-103">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="4f5f4-103">ContainsSubjectOrBodyStrings</span></span>

<span data-ttu-id="4f5f4-104">Das **ContainsSubjectOrBodyStrings** -Element gibt die Zeichenfolgen an, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-104">The **ContainsSubjectOrBodyStrings** element indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSubjectOrBodyStrings>
    <String/>
</ContainsSubjectOrBodyStrings>
```

 <span data-ttu-id="4f5f4-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="4f5f4-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f5f4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f5f4-106">Attributes and elements</span></span>

<span data-ttu-id="4f5f4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f5f4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f5f4-108">Attributes</span></span>

<span data-ttu-id="4f5f4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f5f4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f5f4-110">Child elements</span></span>

|<span data-ttu-id="4f5f4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f5f4-111">**Element**</span></span>|<span data-ttu-id="4f5f4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f5f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f5f4-113">String</span><span class="sxs-lookup"><span data-stu-id="4f5f4-113">String</span></span>](string.md) <br/> |<span data-ttu-id="4f5f4-114">Stellt eine Zeichenfolge dar, die entweder im Textkörper oder im Betreff eingehender Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-114">Represents a string that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f5f4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f5f4-115">Parent elements</span></span>

|<span data-ttu-id="4f5f4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f5f4-116">**Element**</span></span>|<span data-ttu-id="4f5f4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f5f4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f5f4-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="4f5f4-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="4f5f4-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="4f5f4-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="4f5f4-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="4f5f4-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f5f4-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="4f5f4-122">Text value</span></span>

<span data-ttu-id="4f5f4-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f5f4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f5f4-124">Remarks</span></span>

<span data-ttu-id="4f5f4-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4f5f4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f5f4-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f5f4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f5f4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f5f4-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4f5f4-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f5f4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4f5f4-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4f5f4-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4f5f4-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f5f4-130">Validation File</span></span>  <br/> |<span data-ttu-id="4f5f4-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4f5f4-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f5f4-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f5f4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f5f4-133">True</span><span class="sxs-lookup"><span data-stu-id="4f5f4-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f5f4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f5f4-134">See also</span></span>



- [<span data-ttu-id="4f5f4-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f5f4-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

