---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: Das UpdatedItemIds-Element gibt den Bezeichner der aktualisierten Erinnerung Elemente.
ms.openlocfilehash: b95ebb20823706e68b1fd66dc64f756808bb7375
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839347"
---
# <a name="updateditemids"></a><span data-ttu-id="f7825-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="f7825-103">UpdatedItemIds</span></span>

<span data-ttu-id="f7825-104">Das **UpdatedItemIds** -Element gibt den Bezeichner der aktualisierten Erinnerung Elemente.</span><span class="sxs-lookup"><span data-stu-id="f7825-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="f7825-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="f7825-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7825-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7825-106">Attributes and elements</span></span>

<span data-ttu-id="f7825-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7825-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7825-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7825-108">Attributes</span></span>

<span data-ttu-id="f7825-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7825-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7825-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7825-110">Child elements</span></span>

[<span data-ttu-id="f7825-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="f7825-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="f7825-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7825-112">Parent elements</span></span>

[<span data-ttu-id="f7825-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="f7825-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="f7825-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7825-114">Remarks</span></span>

<span data-ttu-id="f7825-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f7825-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f7825-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f7825-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="f7825-117">Wenn der [PerformReminderAction](performreminderaction-operation.md) Vorgang nicht erfolgreich abgeschlossen wurde oder keine Änderungen, auf dem Server vorgenommen wurden, wird das **UpdatedItemIds** -Element als einen leeren Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f7825-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f7825-118">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f7825-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7825-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7825-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7825-120">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7825-120">Schema Name</span></span>  <br/> |<span data-ttu-id="f7825-121">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f7825-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f7825-122">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7825-122">Validation File</span></span>  <br/> |<span data-ttu-id="f7825-123">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7825-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7825-124">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f7825-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7825-125">True</span><span class="sxs-lookup"><span data-stu-id="f7825-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7825-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7825-126">See also</span></span>



[<span data-ttu-id="f7825-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="f7825-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="f7825-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7825-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

