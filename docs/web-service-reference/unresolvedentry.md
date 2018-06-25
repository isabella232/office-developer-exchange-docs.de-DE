---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: Das UnresolvedEntry-Element enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben.
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839324"
---
# <a name="unresolvedentry"></a><span data-ttu-id="8c8d0-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="8c8d0-103">UnresolvedEntry</span></span>

<span data-ttu-id="8c8d0-104">Das **UnresolvedEntry** -Element enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="8c8d0-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8c8d0-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="8c8d0-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="8c8d0-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="8c8d0-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="8c8d0-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8c8d0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8c8d0-108">Attributes and elements</span></span>

<span data-ttu-id="8c8d0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c8d0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8c8d0-110">Attributes</span></span>

<span data-ttu-id="8c8d0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c8d0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c8d0-112">Child elements</span></span>

<span data-ttu-id="8c8d0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8c8d0-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c8d0-114">Parent elements</span></span>

|<span data-ttu-id="8c8d0-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c8d0-115">**Element**</span></span>|<span data-ttu-id="8c8d0-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c8d0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c8d0-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8c8d0-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="8c8d0-118">Definiert eine Anforderung zum Auflösen von Names nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8c8d0-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="8c8d0-119">Text value</span></span>

<span data-ttu-id="8c8d0-120">Der Textwert gibt den Namen einer öffentlichen Liste Kontakts oder der Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="8c8d0-121">Die minimale Länge der Zeichenfolge ist ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c8d0-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c8d0-122">Remarks</span></span>

<span data-ttu-id="8c8d0-123">Der Textwert der dieses Element dient zum Auflösen von Namen für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="8c8d0-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="8c8d0-124">Vorname</span><span class="sxs-lookup"><span data-stu-id="8c8d0-124">First name</span></span>
    
- <span data-ttu-id="8c8d0-125">Nachname</span><span class="sxs-lookup"><span data-stu-id="8c8d0-125">Last name</span></span>
    
- <span data-ttu-id="8c8d0-126">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8c8d0-126">Display name</span></span>
    
- <span data-ttu-id="8c8d0-127">Vollständiger name</span><span class="sxs-lookup"><span data-stu-id="8c8d0-127">Full name</span></span>
    
- <span data-ttu-id="8c8d0-128">Office</span><span class="sxs-lookup"><span data-stu-id="8c8d0-128">Office</span></span>
    
- <span data-ttu-id="8c8d0-129">Alias</span><span class="sxs-lookup"><span data-stu-id="8c8d0-129">Alias</span></span>
    
- <span data-ttu-id="8c8d0-130">SMTP-Adresse</span><span class="sxs-lookup"><span data-stu-id="8c8d0-130">SMTP address</span></span>
    
<span data-ttu-id="8c8d0-131">E-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, werden in einem mehrwertigen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="8c8d0-132">Den [ResolveNames Vorgang](resolvenames-operation.md) ausführt eine teilweise Übereinstimmung mit jeder Wert eines Arrays aus, wenn Sie den Routingtyp am Anfang der aufgelöste Name, beispielsweise "sip:User1@Contoso.com" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="8c8d0-133">Wenn Sie eine Routingtyp nicht angeben, wird **ResolveNames** -Vorgang standardmäßig auf den Routingtyp von smtp, es zu einer primären SMTP-Adresse-Eigenschaft entspricht und nicht durchsucht das mehrwertige Array.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="8c8d0-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8c8d0-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c8d0-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8c8d0-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c8d0-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c8d0-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8c8d0-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8c8d0-137">Schema Name</span></span>  <br/> |<span data-ttu-id="8c8d0-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8c8d0-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8c8d0-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8c8d0-139">Validation File</span></span>  <br/> |<span data-ttu-id="8c8d0-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8c8d0-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8c8d0-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8c8d0-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="8c8d0-142">False</span><span class="sxs-lookup"><span data-stu-id="8c8d0-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c8d0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c8d0-143">See also</span></span>



[<span data-ttu-id="8c8d0-144">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8c8d0-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="8c8d0-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8c8d0-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

