---
title: ItemChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChanges
api_type:
- schema
ms.assetid: cd307892-2f69-4494-8325-219bdb5c3ad5
description: Das ItemChanges-Element enthält ein Array von ItemChange-Elemente, die Elemente und die Updates auf Elemente anwenden zu identifizieren.
ms.openlocfilehash: 38fe112441a8773a2d6b494ed57c63341cab2b58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830141"
---
# <a name="itemchanges"></a><span data-ttu-id="7cf25-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="7cf25-103">ItemChanges</span></span>

<span data-ttu-id="7cf25-104">Das **ItemChanges** -Element enthält ein Array von [ItemChange](itemchange.md) -Elemente, die Elemente und die Updates auf Elemente anwenden zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7cf25-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="7cf25-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="7cf25-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="7cf25-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="7cf25-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="7cf25-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="7cf25-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cf25-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf25-108">Attributes and elements</span></span>

<span data-ttu-id="7cf25-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7cf25-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cf25-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="7cf25-110">Attributes</span></span>

<span data-ttu-id="7cf25-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cf25-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cf25-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf25-112">Child elements</span></span>

|<span data-ttu-id="7cf25-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cf25-113">**Element**</span></span>|<span data-ttu-id="7cf25-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cf25-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cf25-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="7cf25-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="7cf25-116">Enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="7cf25-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7cf25-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf25-117">Parent elements</span></span>

|<span data-ttu-id="7cf25-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cf25-118">**Element**</span></span>|<span data-ttu-id="7cf25-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cf25-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cf25-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="7cf25-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="7cf25-121">Definiert eine Anforderung zum Aktualisieren von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="7cf25-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="7cf25-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="7cf25-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cf25-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cf25-123">Remarks</span></span>

<span data-ttu-id="7cf25-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7cf25-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cf25-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7cf25-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cf25-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cf25-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7cf25-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7cf25-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7cf25-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7cf25-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7cf25-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7cf25-129">Validation File</span></span>  <br/> |<span data-ttu-id="7cf25-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7cf25-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7cf25-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7cf25-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cf25-132">False</span><span class="sxs-lookup"><span data-stu-id="7cf25-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cf25-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cf25-133">See also</span></span>



[<span data-ttu-id="7cf25-134">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="7cf25-134">UpdateItem operation</span></span>](updateitem-operation.md)

