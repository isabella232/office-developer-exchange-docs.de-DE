---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: Das EntityExtractionResult-Element gibt die EntityExtractionResult-Eigenschaft eines Elements an.
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758255"
---
# <a name="entityextractionresult"></a><span data-ttu-id="2c110-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="2c110-103">EntityExtractionResult</span></span>

<span data-ttu-id="2c110-104">Das **EntityExtractionResult** -Element gibt die **EntityExtractionResult** -Eigenschaft eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="2c110-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 <span data-ttu-id="2c110-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="2c110-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c110-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c110-106">Attributes and elements</span></span>

<span data-ttu-id="2c110-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c110-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c110-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c110-108">Attributes</span></span>

<span data-ttu-id="2c110-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c110-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c110-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c110-110">Child elements</span></span>

|<span data-ttu-id="2c110-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c110-111">**Element**</span></span>|<span data-ttu-id="2c110-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c110-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c110-113">Adressen (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2c110-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="2c110-114">Gibt ein Array von **AddressEntity** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="2c110-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="2c110-115">"Meetingsuggestions"</span><span class="sxs-lookup"><span data-stu-id="2c110-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="2c110-116">Gibt ein Array von **MeetingSuggestion** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="2c110-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="2c110-117">"Tasksuggestions"</span><span class="sxs-lookup"><span data-stu-id="2c110-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="2c110-118">Gibt ein Array von **TaskSuggestion** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="2c110-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="2c110-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2c110-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="2c110-120">Gibt ein Array von Entitäten für e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2c110-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="2c110-121">Kontakte (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="2c110-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="2c110-122">Gibt ein Array von Kontakten.</span><span class="sxs-lookup"><span data-stu-id="2c110-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="2c110-123">URLs (ArrayOfUrlEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2c110-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="2c110-124">Gibt ein Array von URLs.</span><span class="sxs-lookup"><span data-stu-id="2c110-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="2c110-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2c110-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="2c110-126">Gibt ein Array von Rufnummern.</span><span class="sxs-lookup"><span data-stu-id="2c110-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c110-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c110-127">Parent elements</span></span>

|<span data-ttu-id="2c110-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c110-128">**Element**</span></span>|<span data-ttu-id="2c110-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c110-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c110-130">Item</span><span class="sxs-lookup"><span data-stu-id="2c110-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="2c110-131">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="2c110-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c110-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c110-132">Remarks</span></span>

<span data-ttu-id="2c110-133">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2c110-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2c110-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2c110-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c110-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2c110-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c110-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c110-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c110-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c110-137">Schema Name</span></span>  <br/> |<span data-ttu-id="2c110-138">Typschema</span><span class="sxs-lookup"><span data-stu-id="2c110-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="2c110-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c110-139">Validation File</span></span>  <br/> |<span data-ttu-id="2c110-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c110-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c110-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2c110-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2c110-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c110-142">See also</span></span>



- [<span data-ttu-id="2c110-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c110-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

