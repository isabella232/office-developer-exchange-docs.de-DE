---
title: Unterhaltung (ConversationRequestType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: Das Conversation-Element stellt eine einzelne Unterhaltung dar, die in einer GetConversationItems-Antwort zurückgegeben wird.
ms.openlocfilehash: 925fd6fce83cad36f4a0e95bb6228ba65e4e9c43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466780"
---
# <a name="conversation-conversationrequesttype"></a><span data-ttu-id="82504-103">Unterhaltung (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="82504-103">Conversation (ConversationRequestType)</span></span>

<span data-ttu-id="82504-104">Das **Conversation** -Element stellt eine einzelne Unterhaltung dar, die in einer **GetConversationItems** -Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82504-104">The **Conversation** element represents a single conversation returned in a **GetConversationItems** response.</span></span> 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="82504-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="82504-105">Attributes and elements</span></span>

<span data-ttu-id="82504-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="82504-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82504-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="82504-107">Attributes</span></span>

<span data-ttu-id="82504-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="82504-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82504-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82504-109">Child elements</span></span>

<span data-ttu-id="82504-110">[Konversations-Nr](conversationid.md)  |  [Von "SyncState (base64Binary)](syncstate-base64binary.md)</span><span class="sxs-lookup"><span data-stu-id="82504-110">[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82504-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82504-111">Parent elements</span></span>

[<span data-ttu-id="82504-112">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="82504-112">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="82504-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82504-113">Remarks</span></span>

<span data-ttu-id="82504-114">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="82504-114">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="82504-115">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="82504-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82504-116">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="82504-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82504-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="82504-117">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82504-118">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="82504-118">Schema name</span></span>  <br/> |<span data-ttu-id="82504-119">Schematypen</span><span class="sxs-lookup"><span data-stu-id="82504-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="82504-120">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="82504-120">Validation file</span></span>  <br/> |<span data-ttu-id="82504-121">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="82504-121">types.xsd</span></span>  <br/> |
|<span data-ttu-id="82504-122">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="82504-122">Can be empty</span></span>  <br/> |<span data-ttu-id="82504-123">False</span><span class="sxs-lookup"><span data-stu-id="82504-123">false</span></span>  <br/> |
   

