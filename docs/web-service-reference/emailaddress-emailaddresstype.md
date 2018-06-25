---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: Das EmailAddress-Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugeordneten Rolle.
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758158"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="6200a-103">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="6200a-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="6200a-104">Das **EmailAddress** -Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="6200a-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="6200a-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="6200a-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6200a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6200a-106">Attributes and elements</span></span>

<span data-ttu-id="6200a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6200a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6200a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6200a-108">Attributes</span></span>

<span data-ttu-id="6200a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6200a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6200a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6200a-110">Child elements</span></span>

|<span data-ttu-id="6200a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6200a-111">**Element**</span></span>|<span data-ttu-id="6200a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6200a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6200a-113">Name (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="6200a-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="6200a-114">Gibt einen Suchbegriff Einschränkung und Schlüssel oder den Namen eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="6200a-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="6200a-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="6200a-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="6200a-116">Definiert die primäre SMTP-Adresse eines Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="6200a-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="6200a-117">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="6200a-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="6200a-118">Gibt an, welche routing von e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6200a-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="6200a-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="6200a-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="6200a-120">Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6200a-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="6200a-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="6200a-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6200a-122">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="6200a-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6200a-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6200a-123">Parent elements</span></span>

|<span data-ttu-id="6200a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6200a-124">**Element**</span></span>|<span data-ttu-id="6200a-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6200a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6200a-126">Rolle</span><span class="sxs-lookup"><span data-stu-id="6200a-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="6200a-127">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6200a-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6200a-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="6200a-128">Text value</span></span>

<span data-ttu-id="6200a-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="6200a-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6200a-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6200a-130">Remarks</span></span>

<span data-ttu-id="6200a-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6200a-131">This element is optional.</span></span>
  
<span data-ttu-id="6200a-132">Das **EmailAddress** -Element ist für Clients, die Exchange Online und Versionen von Microsoft Exchange Server beginnend mit Exchange 2013 abzielen.</span><span class="sxs-lookup"><span data-stu-id="6200a-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6200a-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6200a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6200a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6200a-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6200a-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6200a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="6200a-136">Typschema</span><span class="sxs-lookup"><span data-stu-id="6200a-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="6200a-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6200a-137">Validation File</span></span>  <br/> |<span data-ttu-id="6200a-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6200a-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6200a-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6200a-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6200a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6200a-140">See also</span></span>

- [<span data-ttu-id="6200a-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6200a-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

