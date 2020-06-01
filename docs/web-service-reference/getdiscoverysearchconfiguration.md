---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: Das GetDiscoverySearchConfiguration-Element gibt eine Anforderung zum Abrufen der eDiscovery-Suchkonfiguration an.
ms.openlocfilehash: 821c5e1429c160e326f6d99df3ff4fcc831b83d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461002"
---
# <a name="getdiscoverysearchconfiguration"></a><span data-ttu-id="50d37-103">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="50d37-103">GetDiscoverySearchConfiguration</span></span>

<span data-ttu-id="50d37-104">Das **GetDiscoverySearchConfiguration** -Element gibt eine Anforderung zum Abrufen der eDiscovery-Suchkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="50d37-104">The **GetDiscoverySearchConfiguration** element specifies a request to retrieve the eDiscovery search configuration.</span></span> 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 <span data-ttu-id="50d37-105">**GetDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="50d37-105">**GetDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50d37-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50d37-106">Attributes and elements</span></span>

<span data-ttu-id="50d37-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50d37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50d37-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50d37-108">Attributes</span></span>

<span data-ttu-id="50d37-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50d37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50d37-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50d37-110">Child elements</span></span>

|<span data-ttu-id="50d37-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="50d37-111">**Element**</span></span>|<span data-ttu-id="50d37-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50d37-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50d37-113">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="50d37-113">SearchId</span></span>](searchid.md) <br/> |<span data-ttu-id="50d37-114">Gibt den Bezeichner der Suche an.</span><span class="sxs-lookup"><span data-stu-id="50d37-114">Specifies the identifier of the search.</span></span>  <br/> |
|[<span data-ttu-id="50d37-115">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="50d37-115">ExpandGroupMembership</span></span>](expandgroupmembership.md) <br/> |<span data-ttu-id="50d37-116">Enthält einen booleschen Wert, der angibt, ob die Mitgliedschaft der Gruppe, die von einer **GetSearchableMailboxes** -Anforderung zurückgegeben wird, erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="50d37-116">Contains a Boolean value that indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50d37-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50d37-117">Parent elements</span></span>

<span data-ttu-id="50d37-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="50d37-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50d37-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50d37-119">Remarks</span></span>

<span data-ttu-id="50d37-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50d37-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50d37-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="50d37-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50d37-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="50d37-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50d37-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="50d37-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="50d37-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50d37-124">Schema Name</span></span>  <br/> |<span data-ttu-id="50d37-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="50d37-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="50d37-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50d37-126">Validation File</span></span>  <br/> |<span data-ttu-id="50d37-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="50d37-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50d37-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="50d37-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="50d37-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d37-129">See also</span></span>



- [<span data-ttu-id="50d37-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="50d37-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

