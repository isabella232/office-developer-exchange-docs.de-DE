---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: Das Element MailboxScope bestimmt, ob eine Suche oder Fetch für eine Unterhaltung sollten und das primäre Postfach, Archivpostfach oder sowohl die primäre umfassen Postfach zu archivieren.
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830293"
---
# <a name="mailboxscope"></a><span data-ttu-id="b2127-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="b2127-103">MailboxScope</span></span>

<span data-ttu-id="b2127-104">Das Element **MailboxScope** bestimmt, ob eine Suche oder Fetch für eine Unterhaltung sollten und das primäre Postfach, Archivpostfach oder sowohl die primäre umfassen Postfach zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="b2127-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="b2127-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="b2127-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b2127-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b2127-106">Attributes and elements</span></span>

<span data-ttu-id="b2127-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b2127-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2127-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2127-108">Attributes</span></span>

<span data-ttu-id="b2127-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2127-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2127-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2127-110">Child elements</span></span>

<span data-ttu-id="b2127-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2127-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b2127-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2127-112">Parent elements</span></span>

<span data-ttu-id="b2127-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Unterhaltung (ConversationType)](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="b2127-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b2127-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b2127-114">Text value</span></span>

<span data-ttu-id="b2127-115">Der Textwert der **MailboxScope** -Element entspricht der Bereich zum Suchen oder Abrufen von Elementen in einer Unterhaltung über entweder primären Postfächern, archivieren Postfächer oder Primär- und von archivpostfächern.</span><span class="sxs-lookup"><span data-stu-id="b2127-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="b2127-116">Der Textwert **PrimaryOnly** gibt an, einen Bereich, der das primäre Postfach für einen Benutzer abzielt.</span><span class="sxs-lookup"><span data-stu-id="b2127-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="b2127-117">Der Textwert **ArchiveOnly** gibt an, einen Bereich, der das Archivpostfach für einen Benutzer abzielt.</span><span class="sxs-lookup"><span data-stu-id="b2127-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="b2127-118">Der Textwert **aller** gibt an, einen Bereich, der das primäre Postfach und Archivpostfach beruht.</span><span class="sxs-lookup"><span data-stu-id="b2127-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b2127-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2127-119">Remarks</span></span>

<span data-ttu-id="b2127-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b2127-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b2127-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b2127-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2127-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b2127-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2127-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2127-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2127-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b2127-124">Schema name</span></span>  <br/> |<span data-ttu-id="b2127-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b2127-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b2127-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2127-126">Validation file</span></span>  <br/> |<span data-ttu-id="b2127-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2127-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2127-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b2127-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b2127-129">false</span><span class="sxs-lookup"><span data-stu-id="b2127-129">false</span></span>  <br/> |
   

