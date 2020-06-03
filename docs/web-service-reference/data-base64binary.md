---
title: Data (base64Binary)
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
description: Das Data-Element enthält die Daten eines einzelnen exportierten Elements oder eines Elements, das in ein Postfach hochgeladen werden soll.
ms.openlocfilehash: 43ee16ca7caf634756ca00a88715d9834adad92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526970"
---
# <a name="data-base64binary"></a><span data-ttu-id="28896-103">Data (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="28896-103">Data (base64Binary)</span></span>

<span data-ttu-id="28896-104">Das **Data** -Element enthält die Daten eines einzelnen exportierten Elements oder eines Elements, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="28896-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="28896-105">**xs: base64Binary**</span><span class="sxs-lookup"><span data-stu-id="28896-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="28896-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28896-106">Attributes and elements</span></span>

<span data-ttu-id="28896-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28896-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28896-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28896-108">Attributes</span></span>

<span data-ttu-id="28896-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="28896-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28896-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28896-110">Child elements</span></span>

<span data-ttu-id="28896-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="28896-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28896-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28896-112">Parent elements</span></span>

|<span data-ttu-id="28896-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="28896-113">**Element**</span></span>|<span data-ttu-id="28896-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28896-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28896-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28896-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="28896-116">Enthält den Status und die Ergebnisse einer Anforderung zum Exportieren eines einzelnen Post Fach Elements.</span><span class="sxs-lookup"><span data-stu-id="28896-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="28896-117">Element (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="28896-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="28896-118">Stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="28896-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28896-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="28896-119">Text value</span></span>

<span data-ttu-id="28896-120">Das **Data** -Element enthält die Eigenschaftennamen und Werte für ein exportiertes Element oder ein Element, das in ein Postfach hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="28896-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28896-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28896-121">Remarks</span></span>

<span data-ttu-id="28896-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28896-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28896-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28896-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28896-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="28896-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28896-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28896-125">Schema Name</span></span>  <br/> |<span data-ttu-id="28896-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="28896-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="28896-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28896-127">Validation File</span></span>  <br/> |<span data-ttu-id="28896-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="28896-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28896-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28896-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="28896-130">False</span><span class="sxs-lookup"><span data-stu-id="28896-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28896-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28896-131">See also</span></span>

- [<span data-ttu-id="28896-132">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28896-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="28896-133">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28896-133">UploadItems operation</span></span>](uploaditems-operation.md)

