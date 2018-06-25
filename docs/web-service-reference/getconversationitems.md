---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: Das GetConversationItems-Element definiert eine Anforderung zum Abrufen einer Reihe von Elementen, die in der gleichen Unterhaltung wird zusammenhängen.
ms.openlocfilehash: 9be300318a07173e4a8e11e5a6ca78b885de1199
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758606"
---
# <a name="getconversationitems"></a><span data-ttu-id="a01b5-103">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="a01b5-103">GetConversationItems</span></span>

<span data-ttu-id="a01b5-104">Das **GetConversationItems** -Element definiert eine Anforderung zum Abrufen einer Reihe von Elementen, die in der gleichen Unterhaltung wird zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="a01b5-104">The **GetConversationItems** element defines a request to get a set of items that are related by being in the same conversation.</span></span> 
  
```XML
<GetConversationItems>
   <ItemShape/>
   <FoldersToIgnore/>
   <MaxItemsToReturn/>
   <SortOrder/>
   <MailboxScope/>
   <Conversations/>
</GetConversationItems>
```

 <span data-ttu-id="a01b5-105">**GetConversationItemsType**</span><span class="sxs-lookup"><span data-stu-id="a01b5-105">**GetConversationItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a01b5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a01b5-106">Attributes and elements</span></span>

<span data-ttu-id="a01b5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a01b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a01b5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a01b5-108">Attributes</span></span>

<span data-ttu-id="a01b5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a01b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a01b5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a01b5-110">Child elements</span></span>

<span data-ttu-id="a01b5-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Unterhaltungen](conversations-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="a01b5-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Conversations](conversations-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a01b5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a01b5-112">Parent elements</span></span>

<span data-ttu-id="a01b5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a01b5-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a01b5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a01b5-114">Remarks</span></span>

<span data-ttu-id="a01b5-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a01b5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a01b5-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a01b5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a01b5-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a01b5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a01b5-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a01b5-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a01b5-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a01b5-119">Schema name</span></span>  <br/> |<span data-ttu-id="a01b5-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a01b5-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a01b5-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a01b5-121">Validation file</span></span>  <br/> |<span data-ttu-id="a01b5-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a01b5-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a01b5-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a01b5-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a01b5-124">false</span><span class="sxs-lookup"><span data-stu-id="a01b5-124">false</span></span>  <br/> |
   

