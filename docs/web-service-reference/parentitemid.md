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
description: Das ParentItemId-Element identifiziert das übergeordnete Element, das auf eine zugeordnete Anlage verweist.
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465744"
---
# <a name="parentitemid"></a><span data-ttu-id="60fa1-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="60fa1-103">ParentItemId</span></span>

<span data-ttu-id="60fa1-104">Das **ParentItemId** -Element identifiziert das übergeordnete Element, das auf eine zugeordnete Anlage verweist.</span><span class="sxs-lookup"><span data-stu-id="60fa1-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="60fa1-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="60fa1-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="60fa1-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="60fa1-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="60fa1-107">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="60fa1-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="60fa1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60fa1-108">Attributes and elements</span></span>

<span data-ttu-id="60fa1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60fa1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60fa1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="60fa1-110">Attributes</span></span>

|<span data-ttu-id="60fa1-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="60fa1-111">**Attribute**</span></span>|<span data-ttu-id="60fa1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60fa1-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60fa1-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="60fa1-113">**Id**</span></span> <br/> |<span data-ttu-id="60fa1-114">Bezeichnet ein einzelnes Element im Exchange-Informationsspeicher, das einer Anlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60fa1-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="60fa1-115">Dieser Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="60fa1-115">This value is a string.</span></span> <span data-ttu-id="60fa1-116">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60fa1-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="60fa1-117">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="60fa1-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="60fa1-118">Gibt eine nicht angegebene Version eines Elements an, das durch das **ID-** Attribut im Exchange-Informationsspeicher identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="60fa1-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="60fa1-119">Dies wird verwendet, um sicherzustellen, dass ein aktuelles Element verwendet wird, wenn es mit einer Anlage aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="60fa1-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="60fa1-120">Dieser Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="60fa1-120">This value is a string.</span></span> <span data-ttu-id="60fa1-121">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="60fa1-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="60fa1-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60fa1-122">Child elements</span></span>

<span data-ttu-id="60fa1-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="60fa1-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60fa1-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60fa1-124">Parent elements</span></span>

|<span data-ttu-id="60fa1-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="60fa1-125">**Element**</span></span>|<span data-ttu-id="60fa1-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60fa1-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60fa1-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="60fa1-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="60fa1-128">Definiert eine Anforderung zum Erstellen einer Anlage für ein Element in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="60fa1-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="60fa1-129">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="60fa1-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60fa1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60fa1-130">Remarks</span></span>

<span data-ttu-id="60fa1-131">Dieses Element ist im [CreateAttachment-Vorgang](createattachment-operation.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60fa1-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="60fa1-132">Dieses Element ist im Wesentlichen identisch mit dem [ItemID](itemid.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="60fa1-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="60fa1-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="60fa1-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60fa1-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="60fa1-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60fa1-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="60fa1-135">Namespace</span></span>  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="60fa1-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60fa1-136">Schema Name</span></span>  <br/> |<span data-ttu-id="60fa1-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="60fa1-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="60fa1-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60fa1-138">Validation File</span></span>  <br/> |<span data-ttu-id="60fa1-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="60fa1-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="60fa1-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="60fa1-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="60fa1-141">False</span><span class="sxs-lookup"><span data-stu-id="60fa1-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60fa1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60fa1-142">See also</span></span>

- [<span data-ttu-id="60fa1-143">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="60fa1-143">CreateAttachment operation</span></span>](createattachment-operation.md)

