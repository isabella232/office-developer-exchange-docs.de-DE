---
title: HomeAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57fb1b9d-2ba8-4359-ae79-35c0d56a2d0f
description: Das HomeAddresses-Element gibt ein Array von Home-Adressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: d6a1808bf000ac8bca1e2ce7865aa099037c5a5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460890"
---
# <a name="homeaddresses"></a><span data-ttu-id="08fc1-103">HomeAddresses</span><span class="sxs-lookup"><span data-stu-id="08fc1-103">HomeAddresses</span></span>

<span data-ttu-id="08fc1-104">Das **HomeAddresses** -Element gibt ein Array von Home-Adressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="08fc1-104">The **HomeAddresses** element specifies an array of home addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeAddresses>
    <PostalAddressAttributedValue/>
</HomeAddresses>
```

 <span data-ttu-id="08fc1-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="08fc1-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="08fc1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="08fc1-106">Attributes and elements</span></span>

<span data-ttu-id="08fc1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="08fc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08fc1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="08fc1-108">Attributes</span></span>

<span data-ttu-id="08fc1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="08fc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08fc1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="08fc1-110">Child elements</span></span>

|<span data-ttu-id="08fc1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="08fc1-111">**Element**</span></span>|<span data-ttu-id="08fc1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08fc1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08fc1-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="08fc1-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="08fc1-114">Gibt eine Instanz eines Arrays von Postadressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="08fc1-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="08fc1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="08fc1-115">Parent elements</span></span>

|<span data-ttu-id="08fc1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="08fc1-116">**Element**</span></span>|<span data-ttu-id="08fc1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08fc1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08fc1-118">Persona</span><span class="sxs-lookup"><span data-stu-id="08fc1-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="08fc1-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08fc1-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08fc1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08fc1-120">Remarks</span></span>

<span data-ttu-id="08fc1-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="08fc1-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="08fc1-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="08fc1-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08fc1-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="08fc1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08fc1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="08fc1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="08fc1-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="08fc1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="08fc1-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="08fc1-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="08fc1-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="08fc1-127">Validation File</span></span>  <br/> |<span data-ttu-id="08fc1-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="08fc1-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="08fc1-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="08fc1-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="08fc1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08fc1-130">See also</span></span>



- [<span data-ttu-id="08fc1-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="08fc1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

