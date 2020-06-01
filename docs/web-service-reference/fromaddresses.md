---
title: FromAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromAddresses
api_type:
- schema
ms.assetid: b219f315-c20a-4633-af3e-94bd3e4526b6
description: Das FromAddresses-Element gibt die e-Mail-Adressen an, aus denen eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 4fbb44d02f5010c4395cf691cb6160da4dbb6930
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459539"
---
# <a name="fromaddresses"></a><span data-ttu-id="aee09-103">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="aee09-103">FromAddresses</span></span>

<span data-ttu-id="aee09-104">Das **FromAddresses** -Element gibt die e-Mail-Adressen an, aus denen eingehende Nachrichten gesendet werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="aee09-104">The **FromAddresses** element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span> 
  
```XML
<FromAddresses>
   <Address/>
</FromAddresses>
```

 <span data-ttu-id="aee09-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="aee09-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aee09-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-106">Attributes and elements</span></span>

<span data-ttu-id="aee09-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aee09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aee09-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aee09-108">Attributes</span></span>

<span data-ttu-id="aee09-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aee09-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-110">Child elements</span></span>

|<span data-ttu-id="aee09-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aee09-111">**Element**</span></span>|<span data-ttu-id="aee09-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee09-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee09-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="aee09-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="aee09-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="aee09-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aee09-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-115">Parent elements</span></span>

|<span data-ttu-id="aee09-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="aee09-116">**Element**</span></span>|<span data-ttu-id="aee09-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee09-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee09-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="aee09-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="aee09-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="aee09-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="aee09-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="aee09-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="aee09-121">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="aee09-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aee09-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="aee09-122">Text value</span></span>

<span data-ttu-id="aee09-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee09-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aee09-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aee09-124">Remarks</span></span>

<span data-ttu-id="aee09-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="aee09-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aee09-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="aee09-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee09-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="aee09-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aee09-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aee09-128">Schema Name</span></span>  <br/> |<span data-ttu-id="aee09-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="aee09-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aee09-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aee09-130">Validation File</span></span>  <br/> |<span data-ttu-id="aee09-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="aee09-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aee09-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aee09-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="aee09-133">True</span><span class="sxs-lookup"><span data-stu-id="aee09-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee09-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aee09-134">See also</span></span>



- [<span data-ttu-id="aee09-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="aee09-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

