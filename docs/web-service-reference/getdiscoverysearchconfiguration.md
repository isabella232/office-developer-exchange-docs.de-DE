---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: Das GetDiscoverySearchConfiguration-Element gibt eine Anforderung zum Abrufen der eDiscovery-Suche-Konfiguration.
ms.openlocfilehash: 41a3cabb2822c4ee6a31aa7ff3074d62987edc92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758634"
---
# <a name="getdiscoverysearchconfiguration"></a><span data-ttu-id="dbbdc-103">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbbdc-103">GetDiscoverySearchConfiguration</span></span>

<span data-ttu-id="dbbdc-104">Das **GetDiscoverySearchConfiguration** -Element gibt eine Anforderung zum Abrufen der eDiscovery-Suche-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-104">The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration.</span></span> 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 <span data-ttu-id="dbbdc-105">**GetDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="dbbdc-105">**GetDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dbbdc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dbbdc-106">Attributes and elements</span></span>

<span data-ttu-id="dbbdc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbbdc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dbbdc-108">Attributes</span></span>

<span data-ttu-id="dbbdc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbbdc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbbdc-110">Child elements</span></span>

|<span data-ttu-id="dbbdc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dbbdc-111">**Element**</span></span>|<span data-ttu-id="dbbdc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbbdc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbbdc-113">Such</span><span class="sxs-lookup"><span data-stu-id="dbbdc-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="dbbdc-114">Gibt den Bezeichner der Suche.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="dbbdc-115">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="dbbdc-115">ExpandGroupMembership</span></span>](expandgroupmembership.md) <br/> |<span data-ttu-id="dbbdc-116">Enthält einen booleschen Wert, der angibt, ob die Mitgliedschaft der Gruppe zurückgegeben, die aus einer Anforderung **GetSearchableMailboxes** erweitert.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-116">Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dbbdc-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbbdc-117">Parent elements</span></span>

<span data-ttu-id="dbbdc-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbbdc-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbbdc-119">Remarks</span></span>

<span data-ttu-id="dbbdc-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dbbdc-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dbbdc-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dbbdc-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dbbdc-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbbdc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbbdc-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dbbdc-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dbbdc-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dbbdc-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dbbdc-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="dbbdc-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dbbdc-126">Validation File</span></span>  <br/> |<span data-ttu-id="dbbdc-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dbbdc-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dbbdc-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dbbdc-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dbbdc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbbdc-129">See also</span></span>



- [<span data-ttu-id="dbbdc-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dbbdc-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

