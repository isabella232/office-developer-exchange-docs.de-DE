---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: Das AddressEntity-Element gibt eine einzelne Adressentität.
ms.openlocfilehash: 6a46a64c9824efdd8df6a08fe1a159e7e42b3731
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757250"
---
# <a name="addressentity"></a><span data-ttu-id="8c14d-103">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="8c14d-103">AddressEntity</span></span>

<span data-ttu-id="8c14d-104">Das **AddressEntity** -Element gibt eine einzelne Adressentität.</span><span class="sxs-lookup"><span data-stu-id="8c14d-104">The **AddressEntity** element specifies a single address entity.</span></span> 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 <span data-ttu-id="8c14d-105">**AddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="8c14d-105">**AddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8c14d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8c14d-106">Attributes and elements</span></span>

<span data-ttu-id="8c14d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8c14d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c14d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8c14d-108">Attributes</span></span>

<span data-ttu-id="8c14d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c14d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c14d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c14d-110">Child elements</span></span>

|<span data-ttu-id="8c14d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c14d-111">**Element**</span></span>|<span data-ttu-id="8c14d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c14d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c14d-113">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8c14d-113">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="8c14d-114">Gibt eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="8c14d-114">Specifies an address.</span></span>  <br/> |
|[<span data-ttu-id="8c14d-115">Position</span><span class="sxs-lookup"><span data-stu-id="8c14d-115">Position</span></span>](position.md) <br/> |<span data-ttu-id="8c14d-116">Gibt die Position in einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8c14d-116">Specifies the position in an email message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c14d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c14d-117">Parent elements</span></span>

|<span data-ttu-id="8c14d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c14d-118">**Element**</span></span>|<span data-ttu-id="8c14d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c14d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c14d-120">Adressen (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="8c14d-120">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="8c14d-121">Gibt ein Array von **AddressEntity** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="8c14d-121">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8c14d-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="8c14d-122">Text value</span></span>

<span data-ttu-id="8c14d-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c14d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c14d-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c14d-124">Remarks</span></span>

<span data-ttu-id="8c14d-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c14d-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8c14d-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8c14d-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c14d-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8c14d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c14d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c14d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8c14d-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8c14d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="8c14d-130">Typschema</span><span class="sxs-lookup"><span data-stu-id="8c14d-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="8c14d-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8c14d-131">Validation File</span></span>  <br/> |<span data-ttu-id="8c14d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8c14d-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8c14d-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8c14d-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8c14d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c14d-134">See also</span></span>

- [<span data-ttu-id="8c14d-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8c14d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

