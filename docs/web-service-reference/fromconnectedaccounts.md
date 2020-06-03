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
ms.openlocfilehash: 159ae064827c2f9c2b470580ad5457264e8dae93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464049"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="13fdf-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="13fdf-103">FromConnectedAccounts</span></span>

<span data-ttu-id="13fdf-104">Das **FromConnectedAccounts** -Element darstellt, die Namen der e-Mail-Konten aus denen eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="13fdf-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="13fdf-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="13fdf-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13fdf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13fdf-106">Attributes and elements</span></span>

<span data-ttu-id="13fdf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13fdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13fdf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13fdf-108">Attributes</span></span>

<span data-ttu-id="13fdf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="13fdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13fdf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13fdf-110">Child elements</span></span>

|<span data-ttu-id="13fdf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="13fdf-111">**Element**</span></span>|<span data-ttu-id="13fdf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13fdf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13fdf-113">String</span><span class="sxs-lookup"><span data-stu-id="13fdf-113">String</span></span>](string.md) <br/> |<span data-ttu-id="13fdf-114">Stellt ein E-mail-Konto-Name aus dem eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende zusammengefasst wurden verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="13fdf-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13fdf-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13fdf-115">Parent elements</span></span>

|<span data-ttu-id="13fdf-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="13fdf-116">**Element**</span></span>|<span data-ttu-id="13fdf-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13fdf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13fdf-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="13fdf-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="13fdf-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="13fdf-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="13fdf-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="13fdf-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="13fdf-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="13fdf-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13fdf-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="13fdf-122">Text value</span></span>

<span data-ttu-id="13fdf-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="13fdf-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13fdf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13fdf-124">Remarks</span></span>

<span data-ttu-id="13fdf-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="13fdf-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13fdf-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="13fdf-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13fdf-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="13fdf-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="13fdf-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13fdf-128">Schema Name</span></span>  <br/> |<span data-ttu-id="13fdf-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="13fdf-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="13fdf-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13fdf-130">Validation File</span></span>  <br/> |<span data-ttu-id="13fdf-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="13fdf-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13fdf-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13fdf-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="13fdf-133">True</span><span class="sxs-lookup"><span data-stu-id="13fdf-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13fdf-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13fdf-134">See also</span></span>



- [<span data-ttu-id="13fdf-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="13fdf-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

