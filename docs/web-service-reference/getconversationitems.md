---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: Das GetConversationItems-Element definiert eine Anforderung zum Abrufen einer Gruppe von Elementen, die in der gleichen Unterhaltung miteinander verknüpft sind.
ms.openlocfilehash: cde4bc2c39ccbc51b7436c87c4bc06e3b8d7e52c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457746"
---
# <a name="getconversationitems"></a><span data-ttu-id="57e0c-103">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="57e0c-103">GetConversationItems</span></span>

<span data-ttu-id="57e0c-104">Das **GetConversationItems** -Element definiert eine Anforderung zum Abrufen einer Gruppe von Elementen, die in der gleichen Unterhaltung miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="57e0c-104">The **GetConversationItems** element defines a request to get a set of items that are related by being in the same conversation.</span></span> 
  
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

 <span data-ttu-id="57e0c-105">**GetConversationItemsType**</span><span class="sxs-lookup"><span data-stu-id="57e0c-105">**GetConversationItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57e0c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="57e0c-106">Attributes and elements</span></span>

<span data-ttu-id="57e0c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="57e0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57e0c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="57e0c-108">Attributes</span></span>

<span data-ttu-id="57e0c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="57e0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57e0c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57e0c-110">Child elements</span></span>

<span data-ttu-id="57e0c-111">[ItemShape](itemshape.md)  |  [FoldersToIgnore](folderstoignore.md)  |  [MaxItemsToReturn](maxitemstoreturn.md)  |  [Sortierreihenfolge (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md)  |  [MailboxScope](mailboxscope.md)  |  Unter [Haltungen](conversations-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="57e0c-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Conversations](conversations-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="57e0c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57e0c-112">Parent elements</span></span>

<span data-ttu-id="57e0c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="57e0c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57e0c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57e0c-114">Remarks</span></span>

<span data-ttu-id="57e0c-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="57e0c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="57e0c-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="57e0c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57e0c-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="57e0c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57e0c-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="57e0c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57e0c-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="57e0c-119">Schema name</span></span>  <br/> |<span data-ttu-id="57e0c-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="57e0c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="57e0c-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="57e0c-121">Validation file</span></span>  <br/> |<span data-ttu-id="57e0c-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="57e0c-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57e0c-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="57e0c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="57e0c-124">false</span><span class="sxs-lookup"><span data-stu-id="57e0c-124">false</span></span>  <br/> |
   

