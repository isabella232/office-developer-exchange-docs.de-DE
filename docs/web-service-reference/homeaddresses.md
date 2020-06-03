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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460890"
---
# <a name="homeaddresses"></a><span data-ttu-id="84a76-103">HomeAddresses</span><span class="sxs-lookup"><span data-stu-id="84a76-103">HomeAddresses</span></span>

<span data-ttu-id="84a76-104">Das **HomeAddresses** -Element gibt ein Array von Home-Adressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="84a76-104">The **HomeAddresses** element specifies an array of home addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeAddresses>
    <PostalAddressAttributedValue/>
</HomeAddresses>
```

 <span data-ttu-id="84a76-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="84a76-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84a76-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="84a76-106">Attributes and elements</span></span>

<span data-ttu-id="84a76-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="84a76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84a76-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="84a76-108">Attributes</span></span>

<span data-ttu-id="84a76-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="84a76-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84a76-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84a76-110">Child elements</span></span>

|<span data-ttu-id="84a76-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="84a76-111">**Element**</span></span>|<span data-ttu-id="84a76-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84a76-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84a76-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="84a76-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="84a76-114">Gibt eine Instanz eines Arrays von Postadressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="84a76-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84a76-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84a76-115">Parent elements</span></span>

|<span data-ttu-id="84a76-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="84a76-116">**Element**</span></span>|<span data-ttu-id="84a76-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84a76-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84a76-118">Persona</span><span class="sxs-lookup"><span data-stu-id="84a76-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="84a76-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="84a76-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84a76-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84a76-120">Remarks</span></span>

<span data-ttu-id="84a76-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="84a76-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="84a76-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="84a76-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84a76-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="84a76-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84a76-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="84a76-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84a76-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="84a76-125">Schema Name</span></span>  <br/> |<span data-ttu-id="84a76-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="84a76-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="84a76-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="84a76-127">Validation File</span></span>  <br/> |<span data-ttu-id="84a76-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="84a76-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="84a76-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="84a76-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="84a76-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a76-130">See also</span></span>



- [<span data-ttu-id="84a76-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="84a76-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

