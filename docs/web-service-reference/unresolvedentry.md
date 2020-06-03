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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459840"
---
# <a name="unresolvedentry"></a><span data-ttu-id="2fc51-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="2fc51-103">UnresolvedEntry</span></span>

<span data-ttu-id="2fc51-104">Das **UnresolvedEntry** -Element enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fc51-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="2fc51-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2fc51-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="2fc51-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="2fc51-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="2fc51-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="2fc51-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fc51-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2fc51-108">Attributes and elements</span></span>

<span data-ttu-id="2fc51-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2fc51-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fc51-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="2fc51-110">Attributes</span></span>

<span data-ttu-id="2fc51-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2fc51-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fc51-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2fc51-112">Child elements</span></span>

<span data-ttu-id="2fc51-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2fc51-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2fc51-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2fc51-114">Parent elements</span></span>

|<span data-ttu-id="2fc51-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2fc51-115">**Element**</span></span>|<span data-ttu-id="2fc51-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fc51-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fc51-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2fc51-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="2fc51-118">Definiert eine Anforderung zum Auflösen eindeutiger Namen.</span><span class="sxs-lookup"><span data-stu-id="2fc51-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2fc51-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="2fc51-119">Text value</span></span>

<span data-ttu-id="2fc51-120">Der Wert Text stellt den Namen eines öffentlichen Kontakts oder einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="2fc51-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="2fc51-121">Die minimale Länge der Zeichenfolge ist ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2fc51-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fc51-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fc51-122">Remarks</span></span>

<span data-ttu-id="2fc51-123">Der Textwert dieses Elements wird zum Auflösen von Namen in den folgenden Feldern verwendet:</span><span class="sxs-lookup"><span data-stu-id="2fc51-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="2fc51-124">Vorname</span><span class="sxs-lookup"><span data-stu-id="2fc51-124">First name</span></span>
    
- <span data-ttu-id="2fc51-125">Nachname</span><span class="sxs-lookup"><span data-stu-id="2fc51-125">Last name</span></span>
    
- <span data-ttu-id="2fc51-126">Distinguished Name (DN)</span><span class="sxs-lookup"><span data-stu-id="2fc51-126">Display name</span></span>
    
- <span data-ttu-id="2fc51-127">Vollständiger Name</span><span class="sxs-lookup"><span data-stu-id="2fc51-127">Full name</span></span>
    
- <span data-ttu-id="2fc51-128">Office</span><span class="sxs-lookup"><span data-stu-id="2fc51-128">Office</span></span>
    
- <span data-ttu-id="2fc51-129">Alias</span><span class="sxs-lookup"><span data-stu-id="2fc51-129">Alias</span></span>
    
- <span data-ttu-id="2fc51-130">SMTP-Adresse</span><span class="sxs-lookup"><span data-stu-id="2fc51-130">SMTP address</span></span>
    
<span data-ttu-id="2fc51-131">E-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP werden in einem mehrwertigen Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2fc51-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="2fc51-132">Der [ResolveNames-Vorgang](resolvenames-operation.md) führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens hinzufügen, beispielsweise "SIP:user1@contoso.com".</span><span class="sxs-lookup"><span data-stu-id="2fc51-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="2fc51-133">Wenn Sie keinen Routingtyp angeben, wird der **ResolveNames** -Vorgang standardmäßig auf den Routingtyp von SMTP festgelegt, mit einer primären SMTP-Adress Eigenschaft abgeglichen und nicht mit dem mehrwertigen Array durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2fc51-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="2fc51-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2fc51-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fc51-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2fc51-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fc51-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fc51-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2fc51-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2fc51-137">Schema Name</span></span>  <br/> |<span data-ttu-id="2fc51-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2fc51-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2fc51-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2fc51-139">Validation File</span></span>  <br/> |<span data-ttu-id="2fc51-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2fc51-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2fc51-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2fc51-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="2fc51-142">False</span><span class="sxs-lookup"><span data-stu-id="2fc51-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fc51-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fc51-143">See also</span></span>



[<span data-ttu-id="2fc51-144">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2fc51-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="2fc51-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2fc51-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

