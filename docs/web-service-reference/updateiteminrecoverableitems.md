---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: Das UpdateItemInRecoverableItems-Element gibt eine Anforderung zum Aktualisieren eines Elements in wiederherstellbare Elemente.
ms.openlocfilehash: 768de4bb8abe4780ab520405bae3149b8f17637c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839373"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="0b8bb-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="0b8bb-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="0b8bb-104">Das **UpdateItemInRecoverableItems** -Element gibt eine Anforderung zum Aktualisieren eines Elements in wiederherstellbare Elemente.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="0b8bb-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="0b8bb-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b8bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b8bb-106">Attributes and elements</span></span>

<span data-ttu-id="0b8bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b8bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b8bb-108">Attributes</span></span>

<span data-ttu-id="0b8bb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b8bb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b8bb-110">Child elements</span></span>

<span data-ttu-id="0b8bb-111">[ItemId](itemid.md) | [Updates (Element)](updates-item.md) | [Anlagen](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="0b8bb-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b8bb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b8bb-112">Parent elements</span></span>

<span data-ttu-id="0b8bb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b8bb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b8bb-114">Remarks</span></span>

<span data-ttu-id="0b8bb-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0b8bb-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0b8bb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b8bb-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0b8bb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b8bb-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b8bb-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0b8bb-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0b8bb-119">Schema name</span></span>  <br/> |<span data-ttu-id="0b8bb-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0b8bb-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0b8bb-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0b8bb-121">Validation file</span></span>  <br/> |<span data-ttu-id="0b8bb-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0b8bb-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b8bb-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0b8bb-123">Can be empty</span></span>  <br/> |<span data-ttu-id="0b8bb-124">false</span><span class="sxs-lookup"><span data-stu-id="0b8bb-124">false</span></span>  <br/> |
   
