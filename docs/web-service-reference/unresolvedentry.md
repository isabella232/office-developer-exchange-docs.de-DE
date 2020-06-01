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
description: Das UnresolvedEntry-Element enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459840"
---
# <a name="unresolvedentry"></a><span data-ttu-id="9c67a-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="9c67a-103">UnresolvedEntry</span></span>

<span data-ttu-id="9c67a-104">Das **UnresolvedEntry** -Element enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c67a-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="9c67a-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="9c67a-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="9c67a-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="9c67a-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="9c67a-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="9c67a-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c67a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9c67a-108">Attributes and elements</span></span>

<span data-ttu-id="9c67a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9c67a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c67a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="9c67a-110">Attributes</span></span>

<span data-ttu-id="9c67a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c67a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c67a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c67a-112">Child elements</span></span>

<span data-ttu-id="9c67a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c67a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9c67a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c67a-114">Parent elements</span></span>

|<span data-ttu-id="9c67a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c67a-115">**Element**</span></span>|<span data-ttu-id="9c67a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c67a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c67a-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="9c67a-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="9c67a-118">Definiert eine Anforderung zum Auflösen eindeutiger Namen.</span><span class="sxs-lookup"><span data-stu-id="9c67a-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9c67a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="9c67a-119">Text value</span></span>

<span data-ttu-id="9c67a-120">Der Wert Text stellt den Namen eines öffentlichen Kontakts oder einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="9c67a-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="9c67a-121">Die minimale Länge der Zeichenfolge ist ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9c67a-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c67a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c67a-122">Remarks</span></span>

<span data-ttu-id="9c67a-123">Der Textwert dieses Elements wird zum Auflösen von Namen in den folgenden Feldern verwendet:</span><span class="sxs-lookup"><span data-stu-id="9c67a-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="9c67a-124">Vorname</span><span class="sxs-lookup"><span data-stu-id="9c67a-124">First name</span></span>
    
- <span data-ttu-id="9c67a-125">Nachname</span><span class="sxs-lookup"><span data-stu-id="9c67a-125">Last name</span></span>
    
- <span data-ttu-id="9c67a-126">Distinguished Name (DN)</span><span class="sxs-lookup"><span data-stu-id="9c67a-126">Display name</span></span>
    
- <span data-ttu-id="9c67a-127">Vollständiger Name</span><span class="sxs-lookup"><span data-stu-id="9c67a-127">Full name</span></span>
    
- <span data-ttu-id="9c67a-128">Office</span><span class="sxs-lookup"><span data-stu-id="9c67a-128">Office</span></span>
    
- <span data-ttu-id="9c67a-129">Alias</span><span class="sxs-lookup"><span data-stu-id="9c67a-129">Alias</span></span>
    
- <span data-ttu-id="9c67a-130">SMTP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9c67a-130">SMTP address</span></span>
    
<span data-ttu-id="9c67a-131">E-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP werden in einem mehrwertigen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9c67a-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="9c67a-132">Der [ResolveNames-Vorgang](resolvenames-operation.md) führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens hinzufügen, beispielsweise "SIP:user1@contoso.com".</span><span class="sxs-lookup"><span data-stu-id="9c67a-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="9c67a-133">Wenn Sie keinen Routingtyp angeben, wird der **ResolveNames** -Vorgang standardmäßig auf den Routingtyp von SMTP festgelegt, mit einer primären SMTP-Adress Eigenschaft abgeglichen und nicht mit dem mehrwertigen Array durchsucht.</span><span class="sxs-lookup"><span data-stu-id="9c67a-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="9c67a-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9c67a-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c67a-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9c67a-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c67a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c67a-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9c67a-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9c67a-137">Schema Name</span></span>  <br/> |<span data-ttu-id="9c67a-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9c67a-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9c67a-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9c67a-139">Validation File</span></span>  <br/> |<span data-ttu-id="9c67a-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9c67a-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9c67a-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9c67a-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c67a-142">False</span><span class="sxs-lookup"><span data-stu-id="9c67a-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c67a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c67a-143">See also</span></span>



[<span data-ttu-id="9c67a-144">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9c67a-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="9c67a-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c67a-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

