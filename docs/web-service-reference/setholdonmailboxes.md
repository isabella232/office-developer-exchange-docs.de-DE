---
title: SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fd5b9f0e-23e8-428c-8168-2d6b4ecd6beb
description: Das SetHoldOnMailboxes-Element enthält eine SetHoldOnMailboxes-Anforderung.
ms.openlocfilehash: 7d226de908c4d5a474129e3e1f2344ec1318f538
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831413"
---
# <a name="setholdonmailboxes"></a><span data-ttu-id="9b38e-103">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="9b38e-103">SetHoldOnMailboxes</span></span>

<span data-ttu-id="9b38e-104">Das **SetHoldOnMailboxes** -Element enthält eine **SetHoldOnMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9b38e-104">The **SetHoldOnMailboxes** element contains a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxes>
   <ActionType/>
   <HoldId/>
   <Query/>
   <Mailboxes/>
   <Language/>
   <IncludeNonIndexableItems/>
   <Deduplication/>
   <InPlaceHoldIdentity/>
</SetHoldOnMailboxes>
```

 <span data-ttu-id="9b38e-105">**SetHoldOnMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="9b38e-105">**SetHoldOnMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b38e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b38e-106">Attributes and elements</span></span>

<span data-ttu-id="9b38e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b38e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b38e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b38e-108">Attributes</span></span>

<span data-ttu-id="9b38e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b38e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b38e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b38e-110">Child elements</span></span>

<span data-ttu-id="9b38e-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Abfrage](query.md) | [Postfächer (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Sprache](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplizierung ](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)</span><span class="sxs-lookup"><span data-stu-id="9b38e-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Query](query.md) | [Mailboxes (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Language](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplication](deduplication.md) | [InPlaceHoldIdentity](inplaceholdidentity.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9b38e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b38e-112">Parent elements</span></span>

<span data-ttu-id="9b38e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b38e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b38e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b38e-114">Remarks</span></span>

<span data-ttu-id="9b38e-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9b38e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9b38e-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9b38e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b38e-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9b38e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b38e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b38e-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b38e-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b38e-119">Schema name</span></span>  <br/> |<span data-ttu-id="9b38e-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9b38e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b38e-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b38e-121">Validation file</span></span>  <br/> |<span data-ttu-id="9b38e-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b38e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b38e-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9b38e-123">Can be empty</span></span>  <br/> ||
   

