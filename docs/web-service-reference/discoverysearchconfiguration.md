---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: Das DiscoverySearchConfiguration-Element gibt die Konfiguration für eDiscovery-Suche.
ms.openlocfilehash: 11bf90d8fe73bb0b308deb7ae51f1443488f87e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758029"
---
# <a name="discoverysearchconfiguration"></a><span data-ttu-id="efb6c-103">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="efb6c-103">DiscoverySearchConfiguration</span></span>

<span data-ttu-id="efb6c-104">Das **DiscoverySearchConfiguration** -Element gibt die Konfiguration für eDiscovery-Suche.</span><span class="sxs-lookup"><span data-stu-id="efb6c-104">The **DiscoverySearchConfiguration** element specifies the configuration for eDiscovery search.</span></span> 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 <span data-ttu-id="efb6c-105">**DiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="efb6c-105">**DiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efb6c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="efb6c-106">Attributes and elements</span></span>

<span data-ttu-id="efb6c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="efb6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efb6c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="efb6c-108">Attributes</span></span>

<span data-ttu-id="efb6c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="efb6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efb6c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="efb6c-110">Child elements</span></span>

|<span data-ttu-id="efb6c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="efb6c-111">**Element**</span></span>|<span data-ttu-id="efb6c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efb6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efb6c-113">Such</span><span class="sxs-lookup"><span data-stu-id="efb6c-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="efb6c-114">Gibt den Bezeichner der Suche.</span><span class="sxs-lookup"><span data-stu-id="efb6c-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="efb6c-115">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="efb6c-115">SearchQuery</span></span>](searchquery.md) <br/> |<span data-ttu-id="efb6c-116">Gibt den Namen einer eDiscovery-Suchabfrage.</span><span class="sxs-lookup"><span data-stu-id="efb6c-116">Specifies the name of an eDiscovery search query.</span></span>  <br/> |
|[<span data-ttu-id="efb6c-117">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="efb6c-117">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="efb6c-118">Enthält eine Liste der Postfächer aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="efb6c-118">Contains a list of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="efb6c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="efb6c-119">Parent elements</span></span>

|<span data-ttu-id="efb6c-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="efb6c-120">**Element**</span></span>|<span data-ttu-id="efb6c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efb6c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efb6c-122">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="efb6c-122">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md) <br/> |<span data-ttu-id="efb6c-123">Gibt ein Array von **DiscoverySearchConfiguration** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="efb6c-123">Specifies an array of **DiscoverySearchConfiguration** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efb6c-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="efb6c-124">Remarks</span></span>

<span data-ttu-id="efb6c-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="efb6c-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="efb6c-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="efb6c-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efb6c-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="efb6c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efb6c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="efb6c-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="efb6c-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="efb6c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="efb6c-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="efb6c-130">Message schema</span></span>  <br/> |
|<span data-ttu-id="efb6c-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="efb6c-131">Validation File</span></span>  <br/> |<span data-ttu-id="efb6c-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="efb6c-132">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="efb6c-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="efb6c-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="efb6c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efb6c-134">See also</span></span>

- [<span data-ttu-id="efb6c-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="efb6c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

