---
title: FromConnectedAccounts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromConnectedAccounts
api_type:
- schema
ms.assetid: d4d7ddd7-078d-4f1a-a26b-22dce0c49f3a
description: Das FromConnectedAccounts -Element darstellt, die Namen der e-Mail-Konten aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.
ms.openlocfilehash: 426e81bbbe96fb5fb4b36506438dc4af4f560eef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758546"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="0211e-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="0211e-103">FromConnectedAccounts</span></span>

<span data-ttu-id="0211e-104">Das **FromConnectedAccounts** -Element darstellt, die Namen der e-Mail-Konten aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="0211e-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="0211e-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="0211e-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0211e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0211e-106">Attributes and elements</span></span>

<span data-ttu-id="0211e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0211e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0211e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0211e-108">Attributes</span></span>

<span data-ttu-id="0211e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0211e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0211e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0211e-110">Child elements</span></span>

|<span data-ttu-id="0211e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0211e-111">**Element**</span></span>|<span data-ttu-id="0211e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0211e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0211e-113">String</span><span class="sxs-lookup"><span data-stu-id="0211e-113">String</span></span>](string.md) <br/> |<span data-ttu-id="0211e-114">Stellt ein E-mail-Konto-Name aus dem eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="0211e-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0211e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0211e-115">Parent elements</span></span>

|<span data-ttu-id="0211e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0211e-116">**Element**</span></span>|<span data-ttu-id="0211e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0211e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0211e-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="0211e-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="0211e-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0211e-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="0211e-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="0211e-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="0211e-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="0211e-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0211e-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="0211e-122">Text value</span></span>

<span data-ttu-id="0211e-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="0211e-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0211e-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0211e-124">Remarks</span></span>

<span data-ttu-id="0211e-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0211e-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0211e-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0211e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0211e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0211e-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0211e-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0211e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0211e-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0211e-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0211e-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0211e-130">Validation File</span></span>  <br/> |<span data-ttu-id="0211e-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0211e-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0211e-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0211e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0211e-133">True</span><span class="sxs-lookup"><span data-stu-id="0211e-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0211e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0211e-134">See also</span></span>



- [<span data-ttu-id="0211e-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0211e-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

