---
title: Kontakt (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: Das Contact-Element gibt einen Kontakt im einheitlichen Kontaktspeicher an.
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461520"
---
# <a name="contact-contacttype"></a><span data-ttu-id="d5dd0-103">Kontakt (ContactType)</span><span class="sxs-lookup"><span data-stu-id="d5dd0-103">Contact (ContactType)</span></span>

<span data-ttu-id="d5dd0-104">Das **Contact** -Element gibt einen Kontakt im einheitlichen Kontaktspeicher an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-104">The **Contact** element specifies a contact in the Unified Contact Store.</span></span> 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 <span data-ttu-id="d5dd0-105">**ContactType**</span><span class="sxs-lookup"><span data-stu-id="d5dd0-105">**ContactType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5dd0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5dd0-106">Attributes and elements</span></span>

<span data-ttu-id="d5dd0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5dd0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5dd0-108">Attributes</span></span>

<span data-ttu-id="d5dd0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5dd0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5dd0-110">Child elements</span></span>

|<span data-ttu-id="d5dd0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5dd0-111">**Element**</span></span>|<span data-ttu-id="d5dd0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5dd0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5dd0-113">PersonName</span><span class="sxs-lookup"><span data-stu-id="d5dd0-113">PersonName</span></span>](personname.md) <br/> |<span data-ttu-id="d5dd0-114">Gibt den Namen eines einzelnen an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-114">Specifies the name of an individual.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-115">Business Name</span><span class="sxs-lookup"><span data-stu-id="d5dd0-115">BusinessName</span></span>](businessname.md) <br/> |<span data-ttu-id="d5dd0-116">Gibt den Namen eines Unternehmens an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-116">Specifies the name of a business.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-117">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="d5dd0-117">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="d5dd0-118">Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-118">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-119">Urls</span><span class="sxs-lookup"><span data-stu-id="d5dd0-119">Urls</span></span>](urls.md) <br/> |<span data-ttu-id="d5dd0-120">Gibt ein Array von URLs für eine Rolle an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-120">Specifies an array of URLs for a persona.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-121">Emails (ArrayOfExtractedEmailAddresses)</span><span class="sxs-lookup"><span data-stu-id="d5dd0-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span></span>](emailaddresses-arrayofextractedemailaddresses.md) <br/> |<span data-ttu-id="d5dd0-122">Gibt ein Array von extrahierten e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-122">Specifies an array of extracted email addresses.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-123">Adressen (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="d5dd0-123">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="d5dd0-124">Gibt ein Array von **Address** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-124">Specifies an array of **Address** elements.</span></span>  <br/> |
|[<span data-ttu-id="d5dd0-125">ContactType</span><span class="sxs-lookup"><span data-stu-id="d5dd0-125">ContactString</span></span>](contactstring.md) <br/> |<span data-ttu-id="d5dd0-126">Gibt den Anzeigenamen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-126">Specifies the display name of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5dd0-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5dd0-127">Parent elements</span></span>

|<span data-ttu-id="d5dd0-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5dd0-128">**Element**</span></span>|<span data-ttu-id="d5dd0-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5dd0-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5dd0-130">Kontakte (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="d5dd0-130">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="d5dd0-131">Gibt ein Array von Kontakten an.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-131">Specifies an array of contacts.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5dd0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5dd0-132">Remarks</span></span>

<span data-ttu-id="d5dd0-133">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d5dd0-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5dd0-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d5dd0-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5dd0-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5dd0-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5dd0-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5dd0-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d5dd0-138">Typschema</span><span class="sxs-lookup"><span data-stu-id="d5dd0-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="d5dd0-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5dd0-139">Validation File</span></span>  <br/> |<span data-ttu-id="d5dd0-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d5dd0-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5dd0-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d5dd0-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d5dd0-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5dd0-142">See also</span></span>



- [<span data-ttu-id="d5dd0-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d5dd0-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

