---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: Das GetNonIndexableItemStatistics-Element gibt eine Anforderung zum Nonindexable Element Statistiken abrufen.
ms.openlocfilehash: 4e6f9a0ba94e9946a3910661810bc2c9e748ba9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758740"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="ec036-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="ec036-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="ec036-104">Das **GetNonIndexableItemStatistics** -Element gibt eine Anforderung zum Nonindexable Element Statistiken abrufen.</span><span class="sxs-lookup"><span data-stu-id="ec036-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="ec036-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="ec036-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec036-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec036-106">Attributes and elements</span></span>

<span data-ttu-id="ec036-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec036-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec036-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec036-108">Attributes</span></span>

<span data-ttu-id="ec036-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec036-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec036-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec036-110">Child elements</span></span>

|<span data-ttu-id="ec036-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec036-111">**Element**</span></span>|<span data-ttu-id="ec036-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec036-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec036-113">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="ec036-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="ec036-114">Gibt ein Array von Elementen des **Postfachs** an.</span><span class="sxs-lookup"><span data-stu-id="ec036-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec036-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec036-115">Parent elements</span></span>

<span data-ttu-id="ec036-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec036-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec036-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec036-117">Remarks</span></span>

<span data-ttu-id="ec036-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ec036-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ec036-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ec036-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec036-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec036-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec036-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec036-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec036-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec036-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ec036-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ec036-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="ec036-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec036-124">Validation File</span></span>  <br/> |<span data-ttu-id="ec036-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec036-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec036-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ec036-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ec036-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec036-127">See also</span></span>



- [<span data-ttu-id="ec036-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec036-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

