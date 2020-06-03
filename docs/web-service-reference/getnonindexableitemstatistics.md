---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: Das GetNonIndexableItemStatistics-Element gibt eine Anforderung zum Abrufen von nicht indizierten Element Statistiken an.
ms.openlocfilehash: 4b605379f20f5558566f1cfbad9ef1aa33b6fce6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452790"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="d0ad9-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="d0ad9-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="d0ad9-104">Das **GetNonIndexableItemStatistics** -Element gibt eine Anforderung zum Abrufen von nicht indizierten Element Statistiken an.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="d0ad9-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="d0ad9-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0ad9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0ad9-106">Attributes and elements</span></span>

<span data-ttu-id="d0ad9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0ad9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0ad9-108">Attributes</span></span>

<span data-ttu-id="d0ad9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0ad9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0ad9-110">Child elements</span></span>

|<span data-ttu-id="d0ad9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0ad9-111">**Element**</span></span>|<span data-ttu-id="d0ad9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0ad9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0ad9-113">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="d0ad9-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="d0ad9-114">Gibt ein Array von **Post Fach** Elementen an.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0ad9-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0ad9-115">Parent elements</span></span>

<span data-ttu-id="d0ad9-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0ad9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0ad9-117">Remarks</span></span>

<span data-ttu-id="d0ad9-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0ad9-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0ad9-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0ad9-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0ad9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0ad9-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0ad9-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0ad9-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d0ad9-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d0ad9-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="d0ad9-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0ad9-124">Validation File</span></span>  <br/> |<span data-ttu-id="d0ad9-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d0ad9-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0ad9-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d0ad9-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d0ad9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0ad9-127">See also</span></span>



- [<span data-ttu-id="d0ad9-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0ad9-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

