---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: Das ExtendedProperties-Element gibt ein Array von zusätzlichen Eigenschaften an.
ms.openlocfilehash: 36011e0252ed391daefab190d4da679fb3a3f856
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463097"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="7fa7c-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="7fa7c-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="7fa7c-104">Das **ExtendedProperties** -Element gibt ein Array von zusätzlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="7fa7c-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="7fa7c-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fa7c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fa7c-106">Attributes and elements</span></span>

<span data-ttu-id="7fa7c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fa7c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fa7c-108">Attributes</span></span>

<span data-ttu-id="7fa7c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fa7c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fa7c-110">Child elements</span></span>

|<span data-ttu-id="7fa7c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fa7c-111">**Element**</span></span>|<span data-ttu-id="7fa7c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fa7c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa7c-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7fa7c-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="7fa7c-114">Identifiziert erweiterte MAPI-Eigenschaften für Ordner und Elemente.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fa7c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fa7c-115">Parent elements</span></span>

|<span data-ttu-id="7fa7c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fa7c-116">**Element**</span></span>|<span data-ttu-id="7fa7c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fa7c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa7c-118">Imgroup</span><span class="sxs-lookup"><span data-stu-id="7fa7c-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="7fa7c-119">Stellt eine Sofortnachrichten Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="7fa7c-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="7fa7c-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="7fa7c-121">Gibt die ersten 256 Zeichen eines Post Fach Elements für die Vorschau an, ohne das Element zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fa7c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fa7c-122">Remarks</span></span>

<span data-ttu-id="7fa7c-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7fa7c-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7fa7c-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fa7c-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7fa7c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fa7c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fa7c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fa7c-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fa7c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7fa7c-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="7fa7c-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="7fa7c-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fa7c-129">Validation File</span></span>  <br/> |<span data-ttu-id="7fa7c-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7fa7c-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fa7c-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7fa7c-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7fa7c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fa7c-132">See also</span></span>



- [<span data-ttu-id="7fa7c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fa7c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

