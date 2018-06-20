---
title: SentToAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToAddresses
api_type:
- schema
ms.assetid: 086130d2-93b1-4de1-9553-10ec10322a0c
description: Das SentToAddresses-Element gibt an, die E-mail-Adressen, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende an gesendet wurden.
ms.openlocfilehash: c5a4770ff22e08713e5cf40b9a81191d50a2f437
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831358"
---
# <a name="senttoaddresses"></a><span data-ttu-id="b1e0c-103">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="b1e0c-103">SentToAddresses</span></span>

<span data-ttu-id="b1e0c-104">Das **SentToAddresses** -Element gibt an, die E-mail-Adressen, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende an gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-104">The **SentToAddresses** element indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToAddresses>
   <Address/>
</SentToAddresses>
```

 <span data-ttu-id="b1e0c-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="b1e0c-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1e0c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b1e0c-106">Attributes and elements</span></span>

<span data-ttu-id="b1e0c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1e0c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b1e0c-108">Attributes</span></span>

<span data-ttu-id="b1e0c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1e0c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1e0c-110">Child elements</span></span>

|<span data-ttu-id="b1e0c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1e0c-111">**Element**</span></span>|<span data-ttu-id="b1e0c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1e0c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1e0c-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="b1e0c-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="b1e0c-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1e0c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1e0c-115">Parent elements</span></span>

|<span data-ttu-id="b1e0c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1e0c-116">**Element**</span></span>|<span data-ttu-id="b1e0c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1e0c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1e0c-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="b1e0c-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b1e0c-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b1e0c-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="b1e0c-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b1e0c-121">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b1e0c-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="b1e0c-122">Text value</span></span>

<span data-ttu-id="b1e0c-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1e0c-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1e0c-124">Remarks</span></span>

<span data-ttu-id="b1e0c-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b1e0c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1e0c-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b1e0c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1e0c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1e0c-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1e0c-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b1e0c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b1e0c-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b1e0c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1e0c-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b1e0c-130">Validation File</span></span>  <br/> |<span data-ttu-id="b1e0c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1e0c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1e0c-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b1e0c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1e0c-133">True</span><span class="sxs-lookup"><span data-stu-id="b1e0c-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1e0c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1e0c-134">See also</span></span>



- [<span data-ttu-id="b1e0c-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b1e0c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

