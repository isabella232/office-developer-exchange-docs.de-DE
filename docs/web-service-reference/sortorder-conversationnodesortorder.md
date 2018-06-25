---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: Das SortOrder-Element gibt die Sortierreihenfolge für das Ergebnis einer Anforderung GetConversationItems verwendet.
ms.openlocfilehash: 397aead62d32e72f991af783bff02e79a6e4b0fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831520"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="8bf79-103">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="8bf79-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="8bf79-104">Das **SortOrder** -Element gibt die Sortierreihenfolge für das Ergebnis einer Anforderung **GetConversationItems** verwendet.</span><span class="sxs-lookup"><span data-stu-id="8bf79-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="8bf79-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="8bf79-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bf79-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8bf79-106">Attributes and elements</span></span>

<span data-ttu-id="8bf79-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8bf79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bf79-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bf79-108">Attributes</span></span>

<span data-ttu-id="8bf79-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bf79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bf79-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bf79-110">Child elements</span></span>

<span data-ttu-id="8bf79-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bf79-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8bf79-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bf79-112">Parent elements</span></span>

[<span data-ttu-id="8bf79-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="8bf79-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="8bf79-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="8bf79-114">Text value</span></span>

<span data-ttu-id="8bf79-115">Der Textwert des **SortOrder** -Elements ist die Reihenfolge, in denen Unterhaltungen bestellt.</span><span class="sxs-lookup"><span data-stu-id="8bf79-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="8bf79-116">Ein Textwert der **TreeOrderAscending** gibt an, dass die Kommunikation entsprechend der Struktur des Unterhaltung in aufsteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bf79-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="8bf79-117">Ein Textwert der **TreeOrderDescending** gibt an, dass die Kommunikation entsprechend der Struktur des Unterhaltung in absteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bf79-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="8bf79-118">Ein Textwert der **DateOrderAscending** gibt an, dass die Unterhaltungen entsprechend dem Datum Unterhaltung in aufsteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bf79-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="8bf79-119">Ein Textwert der **DateOrderDescending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltung Datum in absteigender Reihenfolge sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bf79-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8bf79-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bf79-120">Remarks</span></span>

<span data-ttu-id="8bf79-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8bf79-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8bf79-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8bf79-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bf79-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8bf79-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bf79-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bf79-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8bf79-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8bf79-125">Schema name</span></span>  <br/> |<span data-ttu-id="8bf79-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8bf79-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8bf79-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8bf79-127">Validation file</span></span>  <br/> |<span data-ttu-id="8bf79-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8bf79-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8bf79-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8bf79-129">Can be empty</span></span>  <br/> ||
   

