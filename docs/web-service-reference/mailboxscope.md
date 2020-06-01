---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: Das MailboxScope-Element gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder sowohl das primäre als auch das Archivpostfach umfassen soll.
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455373"
---
# <a name="mailboxscope"></a><span data-ttu-id="86c8a-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="86c8a-103">MailboxScope</span></span>

<span data-ttu-id="86c8a-104">Das **MailboxScope** -Element gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder sowohl das primäre als auch das Archivpostfach umfassen soll.</span><span class="sxs-lookup"><span data-stu-id="86c8a-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="86c8a-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="86c8a-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="86c8a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86c8a-106">Attributes and elements</span></span>

<span data-ttu-id="86c8a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86c8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86c8a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86c8a-108">Attributes</span></span>

<span data-ttu-id="86c8a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="86c8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86c8a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86c8a-110">Child elements</span></span>

<span data-ttu-id="86c8a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="86c8a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="86c8a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86c8a-112">Parent elements</span></span>

<span data-ttu-id="86c8a-113">[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  Unter [Haltung (conversationtype)](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="86c8a-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="86c8a-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="86c8a-114">Text value</span></span>

<span data-ttu-id="86c8a-115">Der Textwert des **MailboxScope** -Elements ist der Bereich zum Suchen oder erhalten von Elementen in einer Unterhaltung zwischen primären Postfächern, archivpostfächern oder sowohl primären als auch archivpostfächern.</span><span class="sxs-lookup"><span data-stu-id="86c8a-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="86c8a-116">Der Textwert **Switch primaryonly** gibt einen Bereich an, der auf das primäre Postfach eines Benutzers abzielt.</span><span class="sxs-lookup"><span data-stu-id="86c8a-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="86c8a-117">Der Textwert **Switch archiveonly** gibt einen Bereich an, der auf das Archivpostfach für einen Benutzer abzielt.</span><span class="sxs-lookup"><span data-stu-id="86c8a-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="86c8a-118">Ein Textwert von **all** gibt einen Bereich an, der sowohl auf das primäre Postfach als auch auf das Archivpostfach zielt.</span><span class="sxs-lookup"><span data-stu-id="86c8a-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86c8a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c8a-119">Remarks</span></span>

<span data-ttu-id="86c8a-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="86c8a-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="86c8a-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86c8a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86c8a-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="86c8a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86c8a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="86c8a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86c8a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86c8a-124">Schema name</span></span>  <br/> |<span data-ttu-id="86c8a-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="86c8a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86c8a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86c8a-126">Validation file</span></span>  <br/> |<span data-ttu-id="86c8a-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="86c8a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86c8a-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="86c8a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="86c8a-129">false</span><span class="sxs-lookup"><span data-stu-id="86c8a-129">false</span></span>  <br/> |
   

