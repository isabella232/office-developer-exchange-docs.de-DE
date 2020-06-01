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
ms.openlocfilehash: f2f069717a5862adff3349090c35f95499d135f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456955"
---
# <a name="entityextractionresult"></a><span data-ttu-id="35336-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="35336-103">EntityExtractionResult</span></span>

<span data-ttu-id="35336-104">Das **EntityExtractionResult** -Element gibt die **EntityExtractionResult** -Eigenschaft eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="35336-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
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

 <span data-ttu-id="35336-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="35336-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35336-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35336-106">Attributes and elements</span></span>

<span data-ttu-id="35336-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="35336-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35336-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="35336-108">Attributes</span></span>

<span data-ttu-id="35336-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="35336-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35336-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35336-110">Child elements</span></span>

|<span data-ttu-id="35336-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="35336-111">**Element**</span></span>|<span data-ttu-id="35336-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35336-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35336-113">Adressen (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="35336-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="35336-114">Gibt ein Array von **AddressEntity** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="35336-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="35336-115">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="35336-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="35336-116">Gibt ein Array von **MeetingSuggestion** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="35336-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="35336-117">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="35336-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="35336-118">Gibt ein Array von **Task Suggestion** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="35336-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="35336-119">Emails (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="35336-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="35336-120">Gibt ein Array von e-Mail-Adress Entitäten an.</span><span class="sxs-lookup"><span data-stu-id="35336-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="35336-121">Kontakte (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="35336-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="35336-122">Gibt ein Array von Kontakten an.</span><span class="sxs-lookup"><span data-stu-id="35336-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="35336-123">URLs (ArrayOfUrlEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="35336-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="35336-124">Gibt ein Array von URLs an.</span><span class="sxs-lookup"><span data-stu-id="35336-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="35336-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="35336-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="35336-126">Gibt ein Array von Telefonnummern an.</span><span class="sxs-lookup"><span data-stu-id="35336-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="35336-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35336-127">Parent elements</span></span>

|<span data-ttu-id="35336-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="35336-128">**Element**</span></span>|<span data-ttu-id="35336-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35336-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35336-130">Item</span><span class="sxs-lookup"><span data-stu-id="35336-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="35336-131">Stellt ein generisches Element in der Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="35336-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35336-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35336-132">Remarks</span></span>

<span data-ttu-id="35336-133">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="35336-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="35336-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="35336-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35336-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="35336-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35336-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="35336-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35336-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="35336-137">Schema Name</span></span>  <br/> |<span data-ttu-id="35336-138">Typschema</span><span class="sxs-lookup"><span data-stu-id="35336-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="35336-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="35336-139">Validation File</span></span>  <br/> |<span data-ttu-id="35336-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="35336-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="35336-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="35336-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="35336-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35336-142">See also</span></span>



- [<span data-ttu-id="35336-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="35336-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

