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
ms.openlocfilehash: c96ff50cb1204d86abc66829e1c5da7124f407f1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44448352"
---
# <a name="setholdonmailboxes"></a><span data-ttu-id="a2f5a-103">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="a2f5a-103">SetHoldOnMailboxes</span></span>

<span data-ttu-id="a2f5a-104">Das **SetHoldOnMailboxes** -Element enthält eine **SetHoldOnMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-104">The **SetHoldOnMailboxes** element contains a **SetHoldOnMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="a2f5a-105">**SetHoldOnMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="a2f5a-105">**SetHoldOnMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2f5a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a2f5a-106">Attributes and elements</span></span>

<span data-ttu-id="a2f5a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2f5a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a2f5a-108">Attributes</span></span>

<span data-ttu-id="a2f5a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2f5a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2f5a-110">Child elements</span></span>

<span data-ttu-id="a2f5a-111">[Action Type (HoldActionType)](actiontype-holdactiontype.md)  |  [Haltestatus](holdid.md)  |  [Abfrage](query.md)  |  [Postfächer (ArrayOfStringsType)](mailboxes-arrayofstringstype.md)  |  [Sprache](language.md)  |  [IncludeNonIndexableItems](includenonindexableitems.md)  |  [Deduplizierung](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)</span><span class="sxs-lookup"><span data-stu-id="a2f5a-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Query](query.md) | [Mailboxes (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Language](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplication](deduplication.md) | [InPlaceHoldIdentity](inplaceholdidentity.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a2f5a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2f5a-112">Parent elements</span></span>

<span data-ttu-id="a2f5a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2f5a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2f5a-114">Remarks</span></span>

<span data-ttu-id="a2f5a-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a2f5a-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a2f5a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2f5a-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a2f5a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2f5a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2f5a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a2f5a-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a2f5a-119">Schema name</span></span>  <br/> |<span data-ttu-id="a2f5a-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a2f5a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a2f5a-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a2f5a-121">Validation file</span></span>  <br/> |<span data-ttu-id="a2f5a-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a2f5a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a2f5a-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a2f5a-123">Can be empty</span></span>  <br/> ||
   

