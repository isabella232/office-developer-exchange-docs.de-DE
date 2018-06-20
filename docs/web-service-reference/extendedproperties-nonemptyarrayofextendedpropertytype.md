---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: Das Element ExtendedProperties gibt ein Array von zusätzlichen Eigenschaften.
ms.openlocfilehash: b92108ecde63d4a3ac3cc80861c204c4d1950cc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758354"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="9690a-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="9690a-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="9690a-104">Das Element **ExtendedProperties** gibt ein Array von zusätzlichen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9690a-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="9690a-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="9690a-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9690a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9690a-106">Attributes and elements</span></span>

<span data-ttu-id="9690a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9690a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9690a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9690a-108">Attributes</span></span>

<span data-ttu-id="9690a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9690a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9690a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9690a-110">Child elements</span></span>

|<span data-ttu-id="9690a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9690a-111">**Element**</span></span>|<span data-ttu-id="9690a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9690a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9690a-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="9690a-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="9690a-114">Erweiterte MAPI-Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9690a-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9690a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9690a-115">Parent elements</span></span>

|<span data-ttu-id="9690a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9690a-116">**Element**</span></span>|<span data-ttu-id="9690a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9690a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9690a-118">ImGroup</span><span class="sxs-lookup"><span data-stu-id="9690a-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="9690a-119">Stellt eine instant messaging-Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="9690a-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="9690a-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="9690a-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="9690a-121">Gibt die ersten 256 Zeichen für die Vorschau eines Postfachs-Elements ohne Öffnen des Elements an.</span><span class="sxs-lookup"><span data-stu-id="9690a-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9690a-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9690a-122">Remarks</span></span>

<span data-ttu-id="9690a-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9690a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9690a-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9690a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9690a-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9690a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9690a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="9690a-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9690a-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9690a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="9690a-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="9690a-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="9690a-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9690a-129">Validation File</span></span>  <br/> |<span data-ttu-id="9690a-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9690a-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9690a-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9690a-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9690a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9690a-132">See also</span></span>



- [<span data-ttu-id="9690a-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9690a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

