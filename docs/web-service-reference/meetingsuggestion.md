---
title: MeetingSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6012063-eb67-4e83-a4a6-33482685083f
description: Das MeetingSuggestion-Element gibt eine vorgeschlagene Besprechung an.
ms.openlocfilehash: 132ed907886c0ee9f3c4f46cc835d4b4fc6aa621
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466311"
---
# <a name="meetingsuggestion"></a><span data-ttu-id="01c6b-103">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="01c6b-103">MeetingSuggestion</span></span>

<span data-ttu-id="01c6b-104">Das **MeetingSuggestion** -Element gibt eine vorgeschlagene Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="01c6b-104">The **MeetingSuggestion** element specifies a proposed meeting.</span></span> 
  
```XML
<MeetingSuggestion>
   <Attendees/>
   <Location/>
   <Subject/>
   <MeetingString/>
   <StartTime/>
   <EndTime/>
</MeetingSuggestion>
```

 <span data-ttu-id="01c6b-105">**MeetingSuggestionType**</span><span class="sxs-lookup"><span data-stu-id="01c6b-105">**MeetingSuggestionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01c6b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01c6b-106">Attributes and elements</span></span>

<span data-ttu-id="01c6b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01c6b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01c6b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="01c6b-108">Attributes</span></span>

<span data-ttu-id="01c6b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="01c6b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01c6b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01c6b-110">Child elements</span></span>

<span data-ttu-id="01c6b-111">[Teilnehmer](attendees.md)  |  [Speicherort](location.md)  |  [Betreff](subject.md)  |  [Besprechungs Sammlung](meetingstring.md)  |  [Startzeit](starttime.md)  |  [EndTime](endtime.md)</span><span class="sxs-lookup"><span data-stu-id="01c6b-111">[Attendees](attendees.md) | [Location](location.md) | [Subject](subject.md) | [MeetingString](meetingstring.md) | [StartTime](starttime.md) | [EndTime](endtime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01c6b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01c6b-112">Parent elements</span></span>

[<span data-ttu-id="01c6b-113">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="01c6b-113">MeetingSuggestions</span></span>](meetingsuggestions.md)
  
## <a name="remarks"></a><span data-ttu-id="01c6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01c6b-114">Remarks</span></span>

<span data-ttu-id="01c6b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01c6b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="01c6b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="01c6b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01c6b-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="01c6b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01c6b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="01c6b-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01c6b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01c6b-119">Schema name</span></span>  <br/> |<span data-ttu-id="01c6b-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="01c6b-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="01c6b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01c6b-121">Validation file</span></span>  <br/> |<span data-ttu-id="01c6b-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01c6b-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01c6b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="01c6b-123">Can be empty</span></span>  <br/> ||
   

