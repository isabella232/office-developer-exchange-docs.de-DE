---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: Das MailboxHoldStatus-Element gibt den Aufbewahrungs Status des Postfachs an.
ms.openlocfilehash: 2ac575275fc00d2e3ba38cb4ec7335567ee82da6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468810"
---
# <a name="mailboxholdstatus"></a><span data-ttu-id="027cc-103">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="027cc-103">MailboxHoldStatus</span></span>

<span data-ttu-id="027cc-104">Das **MailboxHoldStatus** -Element gibt den Aufbewahrungs Status des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="027cc-104">The **MailboxHoldStatus** element specifies the hold status of the mailbox.</span></span> 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

<span data-ttu-id="027cc-105">**MailboxHoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="027cc-105">**MailboxHoldStatusType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="027cc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="027cc-106">Attributes and elements</span></span>

<span data-ttu-id="027cc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="027cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="027cc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="027cc-108">Attributes</span></span>

<span data-ttu-id="027cc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="027cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="027cc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="027cc-110">Child elements</span></span>

<span data-ttu-id="027cc-111">[Postfach (Zeichenfolge)](mailbox-string.md)  |  [Status (HoldStatusType)](status-holdstatustype.md)  |  [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="027cc-111">[Mailbox (string)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="027cc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="027cc-112">Parent elements</span></span>

[<span data-ttu-id="027cc-113">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="027cc-113">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
  
## <a name="remarks"></a><span data-ttu-id="027cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="027cc-114">Remarks</span></span>

<span data-ttu-id="027cc-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="027cc-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="027cc-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="027cc-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="027cc-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="027cc-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="027cc-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="027cc-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="027cc-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="027cc-119">Schema name</span></span>  <br/> |<span data-ttu-id="027cc-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="027cc-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="027cc-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="027cc-121">Validation file</span></span>  <br/> |<span data-ttu-id="027cc-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="027cc-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="027cc-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="027cc-123">Can be empty</span></span>  <br/> ||
   

