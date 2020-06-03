---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: Das UpdateItemInRecoverableItems-Element gibt eine Anforderung an, ein Element in Wiederherstellungs fähigen Elementen zu aktualisieren.
ms.openlocfilehash: f3dae55097c613b84a80795185baad559e312b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459784"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="1b5da-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="1b5da-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="1b5da-104">Das **UpdateItemInRecoverableItems** -Element gibt eine Anforderung an, ein Element in Wiederherstellungs fähigen Elementen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1b5da-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="1b5da-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="1b5da-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b5da-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1b5da-106">Attributes and elements</span></span>

<span data-ttu-id="1b5da-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1b5da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b5da-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b5da-108">Attributes</span></span>

<span data-ttu-id="1b5da-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b5da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b5da-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b5da-110">Child elements</span></span>

<span data-ttu-id="1b5da-111">[ItemID](itemid.md)  |  [Updates (Element)](updates-item.md)  |  [Anlagen](attachments-ex15websvcsotherref.md)  |  [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="1b5da-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b5da-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b5da-112">Parent elements</span></span>

<span data-ttu-id="1b5da-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b5da-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b5da-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b5da-114">Remarks</span></span>

<span data-ttu-id="1b5da-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1b5da-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1b5da-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1b5da-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b5da-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1b5da-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b5da-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b5da-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1b5da-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1b5da-119">Schema name</span></span>  <br/> |<span data-ttu-id="1b5da-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1b5da-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1b5da-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1b5da-121">Validation file</span></span>  <br/> |<span data-ttu-id="1b5da-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1b5da-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1b5da-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1b5da-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1b5da-124">False</span><span class="sxs-lookup"><span data-stu-id="1b5da-124">false</span></span>  <br/> |
   

