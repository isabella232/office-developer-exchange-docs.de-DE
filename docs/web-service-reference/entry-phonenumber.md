---
title: Eingabe (Faxnummer)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: Das Entry-Element stellt eine Telefonnummer für einen Kontakt dar.
ms.openlocfilehash: 62f7091bb750dc7ca74b1e5637a437e2cdad4f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459637"
---
# <a name="entry-phonenumber"></a><span data-ttu-id="613c8-103">Eingabe (Faxnummer)</span><span class="sxs-lookup"><span data-stu-id="613c8-103">Entry (PhoneNumber)</span></span>

<span data-ttu-id="613c8-104">Das **Entry** -Element stellt eine Telefonnummer für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="613c8-104">The **Entry** element represents a telephone number for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="613c8-105">**PhoneNumberDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="613c8-105">**PhoneNumberDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="613c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="613c8-106">Attributes and elements</span></span>

<span data-ttu-id="613c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="613c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="613c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="613c8-108">Attributes</span></span>

|<span data-ttu-id="613c8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="613c8-109">**Attribute**</span></span>|<span data-ttu-id="613c8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="613c8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="613c8-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="613c8-111">**Key**</span></span> <br/> | <span data-ttu-id="613c8-112">Gibt die Telefonnummer an.</span><span class="sxs-lookup"><span data-stu-id="613c8-112">Identifies the telephone number.</span></span> <span data-ttu-id="613c8-113">Das Key-Attribut ist vom Typ **PhoneNumberKeyType**.</span><span class="sxs-lookup"><span data-stu-id="613c8-113">The Key attribute is of type **PhoneNumberKeyType**.</span></span><br/><br/> <span data-ttu-id="613c8-114">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="613c8-114">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="613c8-115">- AssistantPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-115">-  AssistantPhone</span></span>  <br/><span data-ttu-id="613c8-116">- BusinessFax</span><span class="sxs-lookup"><span data-stu-id="613c8-116">-  BusinessFax</span></span>  <br/><span data-ttu-id="613c8-117">-Businessphone</span><span class="sxs-lookup"><span data-stu-id="613c8-117">-  BusinessPhone</span></span>  <br/><span data-ttu-id="613c8-118">- BusinessPhone2</span><span class="sxs-lookup"><span data-stu-id="613c8-118">-  BusinessPhone2</span></span>  <br/><span data-ttu-id="613c8-119">-Callback</span><span class="sxs-lookup"><span data-stu-id="613c8-119">-  Callback</span></span>  <br/><span data-ttu-id="613c8-120">-CarPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-120">-  CarPhone</span></span>  <br/><span data-ttu-id="613c8-121">- CompanyMainPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-121">-  CompanyMainPhone</span></span>  <br/><span data-ttu-id="613c8-122">- HomeFax</span><span class="sxs-lookup"><span data-stu-id="613c8-122">-  HomeFax</span></span>  <br/><span data-ttu-id="613c8-123">-HomePhone</span><span class="sxs-lookup"><span data-stu-id="613c8-123">-  HomePhone</span></span>  <br/><span data-ttu-id="613c8-124">- HomePhone2</span><span class="sxs-lookup"><span data-stu-id="613c8-124">-  HomePhone2</span></span>  <br/><span data-ttu-id="613c8-125">-ISDN</span><span class="sxs-lookup"><span data-stu-id="613c8-125">-  Isdn</span></span>  <br/><span data-ttu-id="613c8-126">-MobilePhone</span><span class="sxs-lookup"><span data-stu-id="613c8-126">-  MobilePhone</span></span>  <br/><span data-ttu-id="613c8-127">-OtherFax</span><span class="sxs-lookup"><span data-stu-id="613c8-127">-  OtherFax</span></span>  <br/><span data-ttu-id="613c8-128">-OtherTelephone</span><span class="sxs-lookup"><span data-stu-id="613c8-128">-  OtherTelephone</span></span>  <br/><span data-ttu-id="613c8-129">-Pager</span><span class="sxs-lookup"><span data-stu-id="613c8-129">-  Pager</span></span>  <br/><span data-ttu-id="613c8-130">- PrimaryPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-130">-  PrimaryPhone</span></span>  <br/><span data-ttu-id="613c8-131">-RadioPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-131">-  RadioPhone</span></span>  <br/><span data-ttu-id="613c8-132">-Telex</span><span class="sxs-lookup"><span data-stu-id="613c8-132">-  Telex</span></span>  <br/><span data-ttu-id="613c8-133">- TtyTddPhone</span><span class="sxs-lookup"><span data-stu-id="613c8-133">-  TtyTddPhone</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="613c8-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="613c8-134">Child elements</span></span>

<span data-ttu-id="613c8-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="613c8-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="613c8-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="613c8-136">Parent elements</span></span>

|<span data-ttu-id="613c8-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="613c8-137">**Element**</span></span>|<span data-ttu-id="613c8-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="613c8-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="613c8-139">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="613c8-139">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="613c8-140">Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="613c8-140">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="613c8-141">Textwert</span><span class="sxs-lookup"><span data-stu-id="613c8-141">Text value</span></span>

<span data-ttu-id="613c8-142">Ein Textwert, der eine Telefonnummer darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="613c8-142">A text value that represents a telephone number is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="613c8-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="613c8-143">Remarks</span></span>

<span data-ttu-id="613c8-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="613c8-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="613c8-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="613c8-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="613c8-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="613c8-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="613c8-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="613c8-147">Schema name</span></span>  <br/> |<span data-ttu-id="613c8-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="613c8-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="613c8-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="613c8-149">Validation file</span></span>  <br/> |<span data-ttu-id="613c8-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="613c8-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="613c8-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="613c8-151">Can be empty</span></span>  <br/> |<span data-ttu-id="613c8-152">False</span><span class="sxs-lookup"><span data-stu-id="613c8-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="613c8-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="613c8-153">See also</span></span>

- [<span data-ttu-id="613c8-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="613c8-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="613c8-155">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="613c8-155">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="613c8-156">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="613c8-156">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="613c8-157">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="613c8-157">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

