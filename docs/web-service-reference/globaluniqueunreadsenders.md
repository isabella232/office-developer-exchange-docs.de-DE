---
title: GlobalUniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueUnreadSenders
api_type:
- schema
ms.assetid: 490abe30-7608-407a-923b-a4b3ddbca610
description: Das GlobalUniqueUnreadSenders-Element gibt eine Liste aller Personen an, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung für alle Ordner im Postfach ungelesen sind.
ms.openlocfilehash: 5a26053158a262d65993dba4be90888ee97f2112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530818"
---
# <a name="globaluniqueunreadsenders"></a><span data-ttu-id="ab083-103">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="ab083-103">GlobalUniqueUnreadSenders</span></span>

<span data-ttu-id="ab083-104">Das **GlobalUniqueUnreadSenders** -Element gibt eine Liste aller Personen an, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung für alle Ordner im Postfach ungelesen sind.</span><span class="sxs-lookup"><span data-stu-id="ab083-104">The **GlobalUniqueUnreadSenders** element specifies a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="ab083-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ab083-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ab083-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="ab083-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="ab083-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ab083-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="ab083-108">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="ab083-108">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md)
  
```XML
<GlobalUniqueUnreadSenders>
   <String/>
</GlobalUniqueUnreadSenders>
```

 <span data-ttu-id="ab083-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="ab083-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab083-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab083-110">Attributes and elements</span></span>

<span data-ttu-id="ab083-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab083-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab083-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab083-112">Attributes</span></span>

<span data-ttu-id="ab083-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab083-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab083-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab083-114">Child elements</span></span>

|<span data-ttu-id="ab083-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab083-115">**Element**</span></span>|<span data-ttu-id="ab083-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab083-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab083-117">String</span><span class="sxs-lookup"><span data-stu-id="ab083-117">String</span></span>](string.md) <br/> |<span data-ttu-id="ab083-118">Enthält einen einzelnen Unterhaltungs Absender.</span><span class="sxs-lookup"><span data-stu-id="ab083-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab083-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab083-119">Parent elements</span></span>

|<span data-ttu-id="ab083-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab083-120">**Element**</span></span>|<span data-ttu-id="ab083-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab083-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab083-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ab083-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ab083-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="ab083-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ab083-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="ab083-124">Text value</span></span>

<span data-ttu-id="ab083-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab083-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab083-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab083-126">Remarks</span></span>

<span data-ttu-id="ab083-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ab083-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab083-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ab083-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab083-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab083-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab083-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ab083-130">Schema name</span></span>  <br/> |<span data-ttu-id="ab083-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ab083-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab083-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab083-132">Validation file</span></span>  <br/> |<span data-ttu-id="ab083-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ab083-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab083-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ab083-134">Can be empty</span></span>  <br/> |<span data-ttu-id="ab083-135">False</span><span class="sxs-lookup"><span data-stu-id="ab083-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab083-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab083-136">See also</span></span>



[<span data-ttu-id="ab083-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ab083-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="ab083-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ab083-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="ab083-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ab083-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

