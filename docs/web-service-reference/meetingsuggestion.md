---
title: MeetingSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6012063-eb67-4e83-a4a6-33482685083f
description: Das MeetingSuggestion-Element gibt eine vorgeschlagene Besprechung.
ms.openlocfilehash: 35b618b32101ea36c35d87ca0737e4a7e04eb3a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830444"
---
# <a name="meetingsuggestion"></a><span data-ttu-id="667b2-103">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="667b2-103">MeetingSuggestion</span></span>

<span data-ttu-id="667b2-104">Das **MeetingSuggestion** -Element gibt eine vorgeschlagene Besprechung.</span><span class="sxs-lookup"><span data-stu-id="667b2-104">The **MeetingSuggestion** element specifies a proposed meeting.</span></span> 
  
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

 <span data-ttu-id="667b2-105">**MeetingSuggestionType**</span><span class="sxs-lookup"><span data-stu-id="667b2-105">**MeetingSuggestionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="667b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="667b2-106">Attributes and elements</span></span>

<span data-ttu-id="667b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="667b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="667b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="667b2-108">Attributes</span></span>

<span data-ttu-id="667b2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="667b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="667b2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="667b2-110">Child elements</span></span>

<span data-ttu-id="667b2-111">[Teilnehmer](attendees.md) | [Speicherort](location.md) | [Betreff](subject.md) | ["meetingstring"](meetingstring.md) | [StartTime](starttime.md) | [EndTime](endtime.md)</span><span class="sxs-lookup"><span data-stu-id="667b2-111">[Attendees](attendees.md) | [Location](location.md) | [Subject](subject.md) | [MeetingString](meetingstring.md) | [StartTime](starttime.md) | [EndTime](endtime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="667b2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="667b2-112">Parent elements</span></span>

[<span data-ttu-id="667b2-113">"Meetingsuggestions"</span><span class="sxs-lookup"><span data-stu-id="667b2-113">MeetingSuggestions</span></span>](meetingsuggestions.md)
  
## <a name="remarks"></a><span data-ttu-id="667b2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="667b2-114">Remarks</span></span>

<span data-ttu-id="667b2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="667b2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="667b2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="667b2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="667b2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="667b2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="667b2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="667b2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="667b2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="667b2-119">Schema name</span></span>  <br/> |<span data-ttu-id="667b2-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="667b2-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="667b2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="667b2-121">Validation file</span></span>  <br/> |<span data-ttu-id="667b2-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="667b2-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="667b2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="667b2-123">Can be empty</span></span>  <br/> ||
   

