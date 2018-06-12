---
title: DraftItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c228f7e7-6dc8-476d-9b8c-99cd5b6f9f0c
description: Das DraftItemIds-Element enthält ein Array der Element-IDs zu Entwurfselemente in einer Unterhaltung.
ms.openlocfilehash: f6639b20641ff68fff989d2de5fa4ec2c550d5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758105"
---
# <a name="draftitemids"></a><span data-ttu-id="af71f-103">DraftItemIds</span><span class="sxs-lookup"><span data-stu-id="af71f-103">DraftItemIds</span></span>

<span data-ttu-id="af71f-104">Das **DraftItemIds** -Element enthält ein Array der Element-IDs zu Entwurfselemente in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="af71f-104">The **DraftItemIds** element contains an array of item identifiers to draft items in a conversation.</span></span> 
  
```XML
<DraftItemIds>
   <ItemId/>
   <OccirrenceItemId/>
   <RecurringMasterItemId/>
   <RecurringMasterItemIdRanges/>
</DraftItemIds>
```

 <span data-ttu-id="af71f-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="af71f-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af71f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af71f-106">Attributes and elements</span></span>

<span data-ttu-id="af71f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af71f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af71f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="af71f-108">Attributes</span></span>

<span data-ttu-id="af71f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="af71f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af71f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af71f-110">Child elements</span></span>

<span data-ttu-id="af71f-111">[ItemId](itemid.md) | [OccurrenceItemId](occurrenceitemid.md) | [RecurringMasterItemId](recurringmasteritemid.md) | [RecurringMasterItemIdRanges](recurringmasteritemidranges.md)</span><span class="sxs-lookup"><span data-stu-id="af71f-111">[ItemId](itemid.md) | [OccurrenceItemId](occurrenceitemid.md) | [RecurringMasterItemId](recurringmasteritemid.md) | [RecurringMasterItemIdRanges](recurringmasteritemidranges.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af71f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af71f-112">Parent elements</span></span>

[<span data-ttu-id="af71f-113">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="af71f-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="remarks"></a><span data-ttu-id="af71f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af71f-114">Remarks</span></span>

<span data-ttu-id="af71f-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="af71f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="af71f-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="af71f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af71f-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="af71f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af71f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="af71f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af71f-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af71f-119">Schema name</span></span>  <br/> |<span data-ttu-id="af71f-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="af71f-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="af71f-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af71f-121">Validation file</span></span>  <br/> |<span data-ttu-id="af71f-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af71f-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af71f-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="af71f-123">Can be empty</span></span>  <br/> ||
   

