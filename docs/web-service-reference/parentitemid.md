---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: Das ParentItemId-Element identifiziert das übergeordnete Element, das mit Anlage zugeordneten verknüpft.
ms.openlocfilehash: 9bd875ee5ead8b87996288a640e1bb14e3a5e8b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830703"
---
# <a name="parentitemid"></a><span data-ttu-id="55aa2-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="55aa2-103">ParentItemId</span></span>

<span data-ttu-id="55aa2-104">Das **ParentItemId** -Element identifiziert das übergeordnete Element, das mit Anlage zugeordneten verknüpft.</span><span class="sxs-lookup"><span data-stu-id="55aa2-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="55aa2-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="55aa2-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="55aa2-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="55aa2-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="55aa2-107">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="55aa2-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="55aa2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55aa2-108">Attributes and elements</span></span>

<span data-ttu-id="55aa2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55aa2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55aa2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="55aa2-110">Attributes</span></span>

|<span data-ttu-id="55aa2-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55aa2-111">**Attribute**</span></span>|<span data-ttu-id="55aa2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55aa2-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55aa2-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="55aa2-113">**Id**</span></span> <br/> |<span data-ttu-id="55aa2-114">Gibt ein einzelnes Element in der Exchange-Informationsspeicher, die eine Anlage zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="55aa2-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="55aa2-115">Dieser Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="55aa2-115">This value is a string.</span></span> <span data-ttu-id="55aa2-116">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="55aa2-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="55aa2-117">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="55aa2-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="55aa2-118">Identifiziert eine nicht spezifizierte Version eines Elements, das durch das **Id** -Attribut im Exchange-Speicher identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="55aa2-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="55aa2-119">Dies wird verwendet, um sicherzustellen, dass ein aktuelles Element verwendet wird, wenn es mit einer Anlage aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="55aa2-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="55aa2-120">Dieser Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="55aa2-120">This value is a string.</span></span> <span data-ttu-id="55aa2-121">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="55aa2-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55aa2-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55aa2-122">Child elements</span></span>

<span data-ttu-id="55aa2-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="55aa2-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="55aa2-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55aa2-124">Parent elements</span></span>

|<span data-ttu-id="55aa2-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="55aa2-125">**Element**</span></span>|<span data-ttu-id="55aa2-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55aa2-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55aa2-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="55aa2-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="55aa2-128">Definiert eine Anforderung an eine Anlage zu einem Element in einem Postfach zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="55aa2-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="55aa2-129">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="55aa2-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55aa2-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55aa2-130">Remarks</span></span>

<span data-ttu-id="55aa2-131">Dieses Element wird in den [CreateAttachment Vorgang](createattachment-operation.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="55aa2-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="55aa2-132">Dieses Element ist im Wesentlichen identisch mit dem [ItemId](itemid.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="55aa2-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="55aa2-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="55aa2-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55aa2-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="55aa2-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55aa2-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="55aa2-135">Namespace</span></span>  <br/> |[http://schemas.microsoft.com/exchange/services/2006/messages](http://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="55aa2-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55aa2-136">Schema Name</span></span>  <br/> |<span data-ttu-id="55aa2-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="55aa2-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="55aa2-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55aa2-138">Validation File</span></span>  <br/> |<span data-ttu-id="55aa2-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="55aa2-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="55aa2-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="55aa2-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="55aa2-141">False</span><span class="sxs-lookup"><span data-stu-id="55aa2-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55aa2-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55aa2-142">See also</span></span>

- [<span data-ttu-id="55aa2-143">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="55aa2-143">CreateAttachment operation</span></span>](createattachment-operation.md)

