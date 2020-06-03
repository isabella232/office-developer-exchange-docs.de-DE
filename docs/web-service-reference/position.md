---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Das Position-Element gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde.
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465422"
---
# <a name="position"></a><span data-ttu-id="c5f3b-103">Position</span><span class="sxs-lookup"><span data-stu-id="c5f3b-103">Position</span></span>

<span data-ttu-id="c5f3b-104">Das **Position** -Element gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="c5f3b-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="c5f3b-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5f3b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f3b-106">Attributes and elements</span></span>

<span data-ttu-id="c5f3b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5f3b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5f3b-108">Attributes</span></span>

<span data-ttu-id="c5f3b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5f3b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f3b-110">Child elements</span></span>

<span data-ttu-id="c5f3b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5f3b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f3b-112">Parent elements</span></span>

<span data-ttu-id="c5f3b-113">[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Kontakt (ContactType)](contact-contacttype.md)  |  [Telefon (PhoneEntityType)](phone-phoneentitytype.md)  |  [Task Suggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="c5f3b-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c5f3b-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="c5f3b-114">Text value</span></span>

<span data-ttu-id="c5f3b-115">Der Textwert des **Position** -Elements ist die Position, an der eine extrahierte Entität in der Quellnachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="c5f3b-116">Die Textwerte für das **Position** -Element lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c5f3b-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="c5f3b-117">**LatestReply** – die extrahierte Entität stammt aus der letzten Antwort auf die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="c5f3b-118">**Other** -die extrahierte Entität stammt aus einem nicht definierten Teil der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="c5f3b-119">**Betreff** – die extrahierte Entität stammt aus dem Nachrichtenbetreff.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="c5f3b-120">**Signatur** – die extrahierte Entität stammt aus der Nachrichtensignatur.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c5f3b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5f3b-121">Remarks</span></span>

<span data-ttu-id="c5f3b-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5f3b-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5f3b-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c5f3b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5f3b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5f3b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5f3b-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5f3b-126">Schema name</span></span>  <br/> |<span data-ttu-id="c5f3b-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c5f3b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5f3b-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5f3b-128">Validation file</span></span>  <br/> |<span data-ttu-id="c5f3b-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5f3b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5f3b-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c5f3b-130">Can be empty</span></span>  <br/> ||
   

