---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Das Position-Element gibt die Position einer Entität aus einer Nachricht extrahiert haben.
ms.openlocfilehash: 4bd8f3088891e918e13d5ef1ec8e3e5217cb3fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830853"
---
# <a name="position"></a><span data-ttu-id="31ee7-103">Position</span><span class="sxs-lookup"><span data-stu-id="31ee7-103">Position</span></span>

<span data-ttu-id="31ee7-104">Das **Position** -Element gibt die Position einer Entität aus einer Nachricht extrahiert haben.</span><span class="sxs-lookup"><span data-stu-id="31ee7-104">The **Position** element specifies the position of an entity extracted from a message.</span></span> 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 <span data-ttu-id="31ee7-105">**EmailPositionType**</span><span class="sxs-lookup"><span data-stu-id="31ee7-105">**EmailPositionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31ee7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee7-106">Attributes and elements</span></span>

<span data-ttu-id="31ee7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31ee7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31ee7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="31ee7-108">Attributes</span></span>

<span data-ttu-id="31ee7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="31ee7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31ee7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee7-110">Child elements</span></span>

<span data-ttu-id="31ee7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="31ee7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31ee7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee7-112">Parent elements</span></span>

<span data-ttu-id="31ee7-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Kontakt (Kontakttyp den)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md)  |  [ TaskSuggestion](tasksuggestion.md)</span><span class="sxs-lookup"><span data-stu-id="31ee7-113">[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Contact (ContactType)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md) | [TaskSuggestion](tasksuggestion.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="31ee7-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="31ee7-114">Text value</span></span>

<span data-ttu-id="31ee7-115">Der Textwert des **Position** -Elements ist der Speicherort, von dem eine extrahierte Entität in der Quellnachricht stammt.</span><span class="sxs-lookup"><span data-stu-id="31ee7-115">The text value of the **Position** element is the location where an extracted entity originated in the source message.</span></span> <span data-ttu-id="31ee7-116">Die Textwerte für das Element **Position** sind:</span><span class="sxs-lookup"><span data-stu-id="31ee7-116">The text values for the **Position** element are:</span></span> 
  
- <span data-ttu-id="31ee7-117">**LatestReply** - die extrahierte Entität stammt aus der neuesten Antwort auf die Meldung.</span><span class="sxs-lookup"><span data-stu-id="31ee7-117">**LatestReply** - the extracted entity originates from the latest reply to the message.</span></span> 
    
- <span data-ttu-id="31ee7-118">**Andere** - die extrahierte Entität stammt aus einem nicht definierten Teil der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="31ee7-118">**Other** - the extracted entity originates from an undefined part of the message.</span></span> 
    
- <span data-ttu-id="31ee7-119">**Betreff** - die extrahierte Entität stammt aus der Betreff der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="31ee7-119">**Subject** - the extracted entity originates from the message subject.</span></span> 
    
- <span data-ttu-id="31ee7-120">**Signatur** - die extrahierte Entität stammt aus der Nachrichtensignatur.</span><span class="sxs-lookup"><span data-stu-id="31ee7-120">**Signature** - the extracted entity originates from the message signature.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31ee7-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31ee7-121">Remarks</span></span>

<span data-ttu-id="31ee7-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="31ee7-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="31ee7-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="31ee7-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31ee7-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="31ee7-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31ee7-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="31ee7-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31ee7-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31ee7-126">Schema name</span></span>  <br/> |<span data-ttu-id="31ee7-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="31ee7-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="31ee7-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31ee7-128">Validation file</span></span>  <br/> |<span data-ttu-id="31ee7-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31ee7-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31ee7-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="31ee7-130">Can be empty</span></span>  <br/> ||
   

