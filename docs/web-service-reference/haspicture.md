---
title: HasPicture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasPicture
api_type:
- schema
ms.assetid: 922a43fe-01bd-49f2-9261-e00e4699b8da
description: Das HasPicture-Element gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt.
ms.openlocfilehash: 0f0758e38807587d47b9469f40b10bd9c6ea5012
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462437"
---
# <a name="haspicture"></a><span data-ttu-id="88fd4-103">HasPicture</span><span class="sxs-lookup"><span data-stu-id="88fd4-103">HasPicture</span></span>

<span data-ttu-id="88fd4-104">Das **HasPicture** -Element gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="88fd4-104">The **HasPicture** element indicates whether the contact item has a file attachment that represents the contact's picture.</span></span> 
  
[<span data-ttu-id="88fd4-105">Contact</span><span class="sxs-lookup"><span data-stu-id="88fd4-105">Contact</span></span>](contact.md)
  
[<span data-ttu-id="88fd4-106">HasPicture</span><span class="sxs-lookup"><span data-stu-id="88fd4-106">HasPicture</span></span>](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 <span data-ttu-id="88fd4-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="88fd4-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88fd4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88fd4-108">Attributes and elements</span></span>

<span data-ttu-id="88fd4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88fd4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88fd4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="88fd4-110">Attributes</span></span>

<span data-ttu-id="88fd4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="88fd4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88fd4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88fd4-112">Child elements</span></span>

<span data-ttu-id="88fd4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="88fd4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="88fd4-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88fd4-114">Parent elements</span></span>

|<span data-ttu-id="88fd4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="88fd4-115">**Element**</span></span>|<span data-ttu-id="88fd4-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88fd4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88fd4-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="88fd4-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="88fd4-118">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="88fd4-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="88fd4-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="88fd4-119">Text value</span></span>

<span data-ttu-id="88fd4-120">Der Textwert des **HasPicture** -Elements kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="88fd4-120">The text value of the **HasPicture** element can be either **true** or **false**.</span></span> <span data-ttu-id="88fd4-121">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="88fd4-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88fd4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88fd4-122">Remarks</span></span>

<span data-ttu-id="88fd4-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="88fd4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88fd4-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="88fd4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88fd4-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="88fd4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88fd4-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88fd4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="88fd4-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="88fd4-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="88fd4-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88fd4-128">Validation File</span></span>  <br/> |<span data-ttu-id="88fd4-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88fd4-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88fd4-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="88fd4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="88fd4-131">False</span><span class="sxs-lookup"><span data-stu-id="88fd4-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88fd4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88fd4-132">See also</span></span>



- [<span data-ttu-id="88fd4-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="88fd4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

