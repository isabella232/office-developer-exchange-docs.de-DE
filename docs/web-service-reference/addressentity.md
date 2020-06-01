---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: Das AddressEntity-Element gibt eine einzelne Address-Entität an.
ms.openlocfilehash: c597557fe02a9c0ff7ed3c9862e1662cfbae596a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466906"
---
# <a name="addressentity"></a><span data-ttu-id="23e43-103">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="23e43-103">AddressEntity</span></span>

<span data-ttu-id="23e43-104">Das **AddressEntity** -Element gibt eine einzelne Address-Entität an.</span><span class="sxs-lookup"><span data-stu-id="23e43-104">The **AddressEntity** element specifies a single address entity.</span></span> 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 <span data-ttu-id="23e43-105">**AddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="23e43-105">**AddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23e43-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="23e43-106">Attributes and elements</span></span>

<span data-ttu-id="23e43-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="23e43-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23e43-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="23e43-108">Attributes</span></span>

<span data-ttu-id="23e43-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="23e43-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23e43-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23e43-110">Child elements</span></span>

|<span data-ttu-id="23e43-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="23e43-111">**Element**</span></span>|<span data-ttu-id="23e43-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23e43-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23e43-113">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="23e43-113">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="23e43-114">Gibt eine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="23e43-114">Specifies an address.</span></span>  <br/> |
|[<span data-ttu-id="23e43-115">Position</span><span class="sxs-lookup"><span data-stu-id="23e43-115">Position</span></span>](position.md) <br/> |<span data-ttu-id="23e43-116">Gibt die Position in einer e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="23e43-116">Specifies the position in an email message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23e43-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23e43-117">Parent elements</span></span>

|<span data-ttu-id="23e43-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="23e43-118">**Element**</span></span>|<span data-ttu-id="23e43-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23e43-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23e43-120">Adressen (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="23e43-120">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="23e43-121">Gibt ein Array von **AddressEntity** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="23e43-121">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="23e43-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="23e43-122">Text value</span></span>

<span data-ttu-id="23e43-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="23e43-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23e43-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e43-124">Remarks</span></span>

<span data-ttu-id="23e43-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="23e43-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23e43-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="23e43-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23e43-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="23e43-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23e43-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="23e43-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23e43-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="23e43-129">Schema Name</span></span>  <br/> |<span data-ttu-id="23e43-130">Typschema</span><span class="sxs-lookup"><span data-stu-id="23e43-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="23e43-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="23e43-131">Validation File</span></span>  <br/> |<span data-ttu-id="23e43-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="23e43-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="23e43-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="23e43-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="23e43-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23e43-134">See also</span></span>

- [<span data-ttu-id="23e43-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="23e43-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

