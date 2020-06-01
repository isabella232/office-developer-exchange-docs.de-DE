---
title: E-mailemail (e-)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: Das Address-Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugehörige Rolle an.
ms.openlocfilehash: 8b04b75e91cc16be7f88c9a0ac08c5e36855056e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463461"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="fb5fa-103">E-mailemail (e-)</span><span class="sxs-lookup"><span data-stu-id="fb5fa-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="fb5fa-104">Das Address **-Element gibt die voll** ständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugehörige Rolle an.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="fb5fa-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="fb5fa-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb5fa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fb5fa-106">Attributes and elements</span></span>

<span data-ttu-id="fb5fa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb5fa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb5fa-108">Attributes</span></span>

<span data-ttu-id="fb5fa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb5fa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb5fa-110">Child elements</span></span>

|<span data-ttu-id="fb5fa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb5fa-111">**Element**</span></span>|<span data-ttu-id="fb5fa-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb5fa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb5fa-113">Name (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="fb5fa-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="fb5fa-114">Gibt einen Such Einschränkungsnamen oder-Schlüssel oder den Namen eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="fb5fa-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fb5fa-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="fb5fa-116">Definiert die primäre SMTP-Adresse eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="fb5fa-117">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="fb5fa-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="fb5fa-118">Gibt den Routingtyp einer e-Mail-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="fb5fa-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="fb5fa-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="fb5fa-120">Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="fb5fa-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="fb5fa-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fb5fa-122">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb5fa-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb5fa-123">Parent elements</span></span>

|<span data-ttu-id="fb5fa-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb5fa-124">**Element**</span></span>|<span data-ttu-id="fb5fa-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb5fa-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb5fa-126">Persona</span><span class="sxs-lookup"><span data-stu-id="fb5fa-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="fb5fa-127">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb5fa-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="fb5fa-128">Text value</span></span>

<span data-ttu-id="fb5fa-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb5fa-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb5fa-130">Remarks</span></span>

<span data-ttu-id="fb5fa-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-131">This element is optional.</span></span>
  
<span data-ttu-id="fb5fa-132">Das **Email** -Element ist für Clients gültig, die Exchange Online und Versionen von Exchange Server, die mit Exchange 2013 beginnen, abzielen.</span><span class="sxs-lookup"><span data-stu-id="fb5fa-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fb5fa-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fb5fa-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb5fa-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb5fa-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb5fa-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fb5fa-135">Schema Name</span></span>  <br/> |<span data-ttu-id="fb5fa-136">Typschema</span><span class="sxs-lookup"><span data-stu-id="fb5fa-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="fb5fa-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fb5fa-137">Validation File</span></span>  <br/> |<span data-ttu-id="fb5fa-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fb5fa-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb5fa-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fb5fa-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fb5fa-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb5fa-140">See also</span></span>

- [<span data-ttu-id="fb5fa-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fb5fa-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

