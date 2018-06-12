---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: Das MailboxHoldStatus-Element gibt den Sperrstatus des Postfachs an.
ms.openlocfilehash: 6703c909d0a7b4e83e190807fc3202ecd4699e7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830288"
---
# <a name="mailboxholdstatus"></a><span data-ttu-id="77d85-103">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="77d85-103">MailboxHoldStatus</span></span>

<span data-ttu-id="77d85-104">Das **MailboxHoldStatus** -Element gibt den Sperrstatus des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="77d85-104">The **MailboxHoldStatus** element specifies the hold status of the mailbox.</span></span> 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

<span data-ttu-id="77d85-105">**MailboxHoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="77d85-105">**MailboxHoldStatusType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="77d85-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="77d85-106">Attributes and elements</span></span>

<span data-ttu-id="77d85-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="77d85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77d85-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="77d85-108">Attributes</span></span>

<span data-ttu-id="77d85-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="77d85-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77d85-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77d85-110">Child elements</span></span>

<span data-ttu-id="77d85-111">[Postfach (String)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="77d85-111">[Mailbox (string)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="77d85-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77d85-112">Parent elements</span></span>

[<span data-ttu-id="77d85-113">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="77d85-113">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
  
## <a name="remarks"></a><span data-ttu-id="77d85-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77d85-114">Remarks</span></span>

<span data-ttu-id="77d85-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="77d85-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="77d85-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="77d85-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77d85-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="77d85-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77d85-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="77d85-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77d85-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="77d85-119">Schema name</span></span>  <br/> |<span data-ttu-id="77d85-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="77d85-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="77d85-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="77d85-121">Validation file</span></span>  <br/> |<span data-ttu-id="77d85-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77d85-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77d85-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="77d85-123">Can be empty</span></span>  <br/> ||
   

