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
description: Das ItemChanges-Element enthält ein Array von ItemChange-Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.
ms.openlocfilehash: ea6fb2023b88360f9558057e80c7fe0d855173b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459910"
---
# <a name="itemchanges"></a><span data-ttu-id="ae934-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="ae934-103">ItemChanges</span></span>

<span data-ttu-id="ae934-104">Das **ItemChanges** -Element enthält ein Array von [ItemChange](itemchange.md) -Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae934-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="ae934-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ae934-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="ae934-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="ae934-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="ae934-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="ae934-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae934-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ae934-108">Attributes and elements</span></span>

<span data-ttu-id="ae934-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ae934-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae934-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae934-110">Attributes</span></span>

<span data-ttu-id="ae934-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae934-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae934-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae934-112">Child elements</span></span>

|<span data-ttu-id="ae934-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae934-113">**Element**</span></span>|<span data-ttu-id="ae934-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae934-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae934-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="ae934-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="ae934-116">Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae934-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae934-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae934-117">Parent elements</span></span>

|<span data-ttu-id="ae934-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae934-118">**Element**</span></span>|<span data-ttu-id="ae934-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae934-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae934-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ae934-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="ae934-121">Definiert eine Anforderung zum Aktualisieren von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="ae934-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="ae934-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ae934-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae934-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae934-123">Remarks</span></span>

<span data-ttu-id="ae934-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae934-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae934-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ae934-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae934-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae934-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae934-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ae934-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ae934-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ae934-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae934-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ae934-129">Validation File</span></span>  <br/> |<span data-ttu-id="ae934-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ae934-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae934-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ae934-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae934-132">False</span><span class="sxs-lookup"><span data-stu-id="ae934-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae934-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae934-133">See also</span></span>



[<span data-ttu-id="ae934-134">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ae934-134">UpdateItem operation</span></span>](updateitem-operation.md)

