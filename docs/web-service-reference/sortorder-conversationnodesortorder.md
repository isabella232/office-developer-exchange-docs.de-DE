---
title: Sortierreihenfolge (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: Das Element "Sort" gibt die Sortierreihenfolge an, die für das Ergebnis einer GetConversationItems-Anforderung verwendet wird.
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530965"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="47f40-103">Sortierreihenfolge (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="47f40-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="47f40-104">Das **Element "Sort" gibt** die Sortierreihenfolge an, die für das Ergebnis einer **GetConversationItems** -Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47f40-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="47f40-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="47f40-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47f40-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="47f40-106">Attributes and elements</span></span>

<span data-ttu-id="47f40-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="47f40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47f40-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="47f40-108">Attributes</span></span>

<span data-ttu-id="47f40-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="47f40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47f40-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47f40-110">Child elements</span></span>

<span data-ttu-id="47f40-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="47f40-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="47f40-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47f40-112">Parent elements</span></span>

[<span data-ttu-id="47f40-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="47f40-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="47f40-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="47f40-114">Text value</span></span>

<span data-ttu-id="47f40-115">Der Textwert des Elements " **Sortier** Reihenfolge" ist die Reihenfolge, in der Unterhaltungen sortiert wurden.</span><span class="sxs-lookup"><span data-stu-id="47f40-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="47f40-116">Der Textwert **TreeOrderAscending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltungs Struktur in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="47f40-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="47f40-117">Der Textwert **TreeOrderDescending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltungs Struktur in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="47f40-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="47f40-118">Der Textwert **DateOrderAscending** gibt an, dass die Unterhaltungen entsprechend dem Unterhaltungs Datum in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="47f40-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="47f40-119">Der Textwert **DateOrderDescending** gibt an, dass die Unterhaltungen entsprechend dem Unterhaltungs Datum in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="47f40-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="47f40-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47f40-120">Remarks</span></span>

<span data-ttu-id="47f40-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="47f40-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="47f40-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="47f40-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47f40-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="47f40-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47f40-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="47f40-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="47f40-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="47f40-125">Schema name</span></span>  <br/> |<span data-ttu-id="47f40-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="47f40-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="47f40-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="47f40-127">Validation file</span></span>  <br/> |<span data-ttu-id="47f40-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="47f40-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="47f40-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="47f40-129">Can be empty</span></span>  <br/> ||
   

