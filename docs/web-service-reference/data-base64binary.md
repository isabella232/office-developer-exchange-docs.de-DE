---
title: Daten (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: Data-Element enthält die Daten von einem einzelnen exportierten Element oder ein Element in einem Postfach hochladen.
ms.openlocfilehash: 9560273e31a64edb2254489961733dfe7360ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757844"
---
# <a name="data-base64binary"></a><span data-ttu-id="5137b-103">Daten (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="5137b-103">Data (base64Binary)</span></span>

<span data-ttu-id="5137b-104">**Data** -Element enthält die Daten von einem einzelnen exportierten Element oder ein Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="5137b-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="5137b-105">**xs:base64Binary**</span><span class="sxs-lookup"><span data-stu-id="5137b-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5137b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5137b-106">Attributes and elements</span></span>

<span data-ttu-id="5137b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5137b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5137b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5137b-108">Attributes</span></span>

<span data-ttu-id="5137b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5137b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5137b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5137b-110">Child elements</span></span>

<span data-ttu-id="5137b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5137b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5137b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5137b-112">Parent elements</span></span>

|<span data-ttu-id="5137b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5137b-113">**Element**</span></span>|<span data-ttu-id="5137b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5137b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5137b-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5137b-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="5137b-116">Enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach-Element zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="5137b-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="5137b-117">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="5137b-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="5137b-118">Stellt ein einzelnes Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="5137b-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5137b-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5137b-119">Text value</span></span>

<span data-ttu-id="5137b-120">**Data** -Element enthält die Eigenschaftennamen und Werte für eine exportierte Element oder ein Element, das in einem Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5137b-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5137b-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5137b-121">Remarks</span></span>

<span data-ttu-id="5137b-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5137b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5137b-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5137b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5137b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="5137b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5137b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5137b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5137b-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5137b-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="5137b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5137b-127">Validation File</span></span>  <br/> |<span data-ttu-id="5137b-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5137b-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5137b-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5137b-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="5137b-130">False</span><span class="sxs-lookup"><span data-stu-id="5137b-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5137b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5137b-131">See also</span></span>

- [<span data-ttu-id="5137b-132">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5137b-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="5137b-133">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5137b-133">UploadItems operation</span></span>](uploaditems-operation.md)

