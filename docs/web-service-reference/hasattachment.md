---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: HasAttachment-Element gibt einen booleschen Wert, um anzugeben, ob das Element Anlagen enthält.
ms.openlocfilehash: dfe163e0850e835784a43984a34c89f14bfbc59b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829798"
---
# <a name="hasattachment"></a><span data-ttu-id="d94a9-103">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="d94a9-103">HasAttachment</span></span>

<span data-ttu-id="d94a9-104">**HasAttachment** -Element gibt einen booleschen Wert, um anzugeben, ob das Element Anlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="d94a9-104">The **HasAttachment** element specifies a Boolean value to indicate whether the item has attachments.</span></span> 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 <span data-ttu-id="d94a9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d94a9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d94a9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d94a9-106">Attributes and elements</span></span>

<span data-ttu-id="d94a9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d94a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d94a9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d94a9-108">Attributes</span></span>

<span data-ttu-id="d94a9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d94a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d94a9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d94a9-110">Child elements</span></span>

<span data-ttu-id="d94a9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d94a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d94a9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d94a9-112">Parent elements</span></span>

|<span data-ttu-id="d94a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d94a9-113">**Element**</span></span>|<span data-ttu-id="d94a9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d94a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d94a9-115">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="d94a9-115">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="d94a9-116">Gibt die ersten 256 Zeichen für die Vorschau eines Postfachs-Elements ohne Öffnen des Elements an.</span><span class="sxs-lookup"><span data-stu-id="d94a9-116">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d94a9-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d94a9-117">Text value</span></span>

<span data-ttu-id="d94a9-118">Der Textwert **true** für das Element **HasAttachment** gibt an, dass das Element eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="d94a9-118">A text value of **true** for the **HasAttachment** element indicates that the item has an attachment.</span></span> <span data-ttu-id="d94a9-119">Der Wert **false** gibt an, dass das Element eine Anlage nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d94a9-119">A value of **false** indicates that the item does not have an attachment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d94a9-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d94a9-120">Remarks</span></span>

<span data-ttu-id="d94a9-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d94a9-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d94a9-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d94a9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d94a9-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d94a9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d94a9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d94a9-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d94a9-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d94a9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d94a9-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="d94a9-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d94a9-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d94a9-127">Validation File</span></span>  <br/> |<span data-ttu-id="d94a9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d94a9-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d94a9-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d94a9-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d94a9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d94a9-130">See also</span></span>



- [<span data-ttu-id="d94a9-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d94a9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

