---
title: Eintrag ("PhoneNumber")
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
description: Entry-Element stellt eine Telefonnummer für einen Kontakt.
ms.openlocfilehash: 3953488fb0b57fcf01c2fb99039478bbe03c7f5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758259"
---
# <a name="entry-phonenumber"></a><span data-ttu-id="e4e17-103">Eintrag ("PhoneNumber")</span><span class="sxs-lookup"><span data-stu-id="e4e17-103">Entry (PhoneNumber)</span></span>

<span data-ttu-id="e4e17-104">**Entry** -Element stellt eine Telefonnummer für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="e4e17-104">The **Entry** element represents a telephone number for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="e4e17-105">**PhoneNumberDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="e4e17-105">**PhoneNumberDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e4e17-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e4e17-106">Attributes and elements</span></span>

<span data-ttu-id="e4e17-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e4e17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4e17-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e4e17-108">Attributes</span></span>

|<span data-ttu-id="e4e17-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e4e17-109">**Attribute**</span></span>|<span data-ttu-id="e4e17-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4e17-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4e17-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="e4e17-111">**Key**</span></span> <br/> | <span data-ttu-id="e4e17-112">Gibt die Telefonnummer ein.</span><span class="sxs-lookup"><span data-stu-id="e4e17-112">Identifies the telephone number.</span></span> <span data-ttu-id="e4e17-113">Das Key-Attribut ist vom Typ **PhoneNumberKeyType**.</span><span class="sxs-lookup"><span data-stu-id="e4e17-113">The Key attribute is of type **PhoneNumberKeyType**.</span></span><br/><br/> <span data-ttu-id="e4e17-114">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="e4e17-114">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="e4e17-115">-Telefon (Sekretariat)</span><span class="sxs-lookup"><span data-stu-id="e4e17-115">-  AssistantPhone</span></span>  <br/><span data-ttu-id="e4e17-116">-Geschäftlich Fax</span><span class="sxs-lookup"><span data-stu-id="e4e17-116">-  BusinessFax</span></span>  <br/><span data-ttu-id="e4e17-117">-BusinessPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-117">-  BusinessPhone</span></span>  <br/><span data-ttu-id="e4e17-118">-BusinessPhone2</span><span class="sxs-lookup"><span data-stu-id="e4e17-118">-  BusinessPhone2</span></span>  <br/><span data-ttu-id="e4e17-119">-Rückruf</span><span class="sxs-lookup"><span data-stu-id="e4e17-119">-  Callback</span></span>  <br/><span data-ttu-id="e4e17-120">-CarPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-120">-  CarPhone</span></span>  <br/><span data-ttu-id="e4e17-121">-CompanyMainPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-121">-  CompanyMainPhone</span></span>  <br/><span data-ttu-id="e4e17-122">-Fax (privat)</span><span class="sxs-lookup"><span data-stu-id="e4e17-122">-  HomeFax</span></span>  <br/><span data-ttu-id="e4e17-123">-HomePhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-123">-  HomePhone</span></span>  <br/><span data-ttu-id="e4e17-124">-HomePhone2</span><span class="sxs-lookup"><span data-stu-id="e4e17-124">-  HomePhone2</span></span>  <br/><span data-ttu-id="e4e17-125">-Isdn</span><span class="sxs-lookup"><span data-stu-id="e4e17-125">-  Isdn</span></span>  <br/><span data-ttu-id="e4e17-126">-Kontaktdetails</span><span class="sxs-lookup"><span data-stu-id="e4e17-126">-  MobilePhone</span></span>  <br/><span data-ttu-id="e4e17-127">-OtherFax</span><span class="sxs-lookup"><span data-stu-id="e4e17-127">-  OtherFax</span></span>  <br/><span data-ttu-id="e4e17-128">-OtherTelephone</span><span class="sxs-lookup"><span data-stu-id="e4e17-128">-  OtherTelephone</span></span>  <br/><span data-ttu-id="e4e17-129">-Pager</span><span class="sxs-lookup"><span data-stu-id="e4e17-129">-  Pager</span></span>  <br/><span data-ttu-id="e4e17-130">-PrimaryPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-130">-  PrimaryPhone</span></span>  <br/><span data-ttu-id="e4e17-131">-RadioPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-131">-  RadioPhone</span></span>  <br/><span data-ttu-id="e4e17-132">-Telex</span><span class="sxs-lookup"><span data-stu-id="e4e17-132">-  Telex</span></span>  <br/><span data-ttu-id="e4e17-133">-TtyTddPhone</span><span class="sxs-lookup"><span data-stu-id="e4e17-133">-  TtyTddPhone</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e4e17-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e4e17-134">Child elements</span></span>

<span data-ttu-id="e4e17-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="e4e17-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e4e17-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e4e17-136">Parent elements</span></span>

|<span data-ttu-id="e4e17-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="e4e17-137">**Element**</span></span>|<span data-ttu-id="e4e17-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4e17-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4e17-139">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="e4e17-139">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="e4e17-140">Stellt eine Auflistung von Telefonnummern für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="e4e17-140">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e4e17-141">Textwert</span><span class="sxs-lookup"><span data-stu-id="e4e17-141">Text value</span></span>

<span data-ttu-id="e4e17-142">Ein Textwert, der eine Telefonnummer darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4e17-142">A text value that represents a telephone number is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4e17-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4e17-143">Remarks</span></span>

<span data-ttu-id="e4e17-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e4e17-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4e17-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e4e17-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4e17-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4e17-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e4e17-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e4e17-147">Schema name</span></span>  <br/> |<span data-ttu-id="e4e17-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e4e17-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="e4e17-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e4e17-149">Validation file</span></span>  <br/> |<span data-ttu-id="e4e17-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e4e17-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e4e17-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e4e17-151">Can be empty</span></span>  <br/> |<span data-ttu-id="e4e17-152">False</span><span class="sxs-lookup"><span data-stu-id="e4e17-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4e17-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4e17-153">See also</span></span>

- [<span data-ttu-id="e4e17-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e4e17-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e4e17-155">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="e4e17-155">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="e4e17-156">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="e4e17-156">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="e4e17-157">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="e4e17-157">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

