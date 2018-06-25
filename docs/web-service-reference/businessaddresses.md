---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: Das BusinessAddresses-Element gibt ein Array von Business-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: bc7ad948572c24f913ae02abb9e8fc5a7b1e0b0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757481"
---
# <a name="businessaddresses"></a><span data-ttu-id="45a4b-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="45a4b-103">BusinessAddresses</span></span>

<span data-ttu-id="45a4b-104">Das **BusinessAddresses** -Element gibt ein Array von Business-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="45a4b-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="45a4b-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="45a4b-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45a4b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="45a4b-106">Attributes and elements</span></span>

<span data-ttu-id="45a4b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="45a4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45a4b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="45a4b-108">Attributes</span></span>

<span data-ttu-id="45a4b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45a4b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a4b-110">Child elements</span></span>

|<span data-ttu-id="45a4b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="45a4b-111">**Element**</span></span>|<span data-ttu-id="45a4b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45a4b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45a4b-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="45a4b-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="45a4b-114">Gibt eine Instanz eines Arrays von Postanschriften und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="45a4b-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45a4b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a4b-115">Parent elements</span></span>

|<span data-ttu-id="45a4b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="45a4b-116">**Element**</span></span>|<span data-ttu-id="45a4b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45a4b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45a4b-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="45a4b-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="45a4b-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45a4b-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45a4b-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45a4b-120">Remarks</span></span>

<span data-ttu-id="45a4b-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="45a4b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="45a4b-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="45a4b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45a4b-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="45a4b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45a4b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="45a4b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45a4b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="45a4b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="45a4b-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="45a4b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="45a4b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="45a4b-127">Validation File</span></span>  <br/> |<span data-ttu-id="45a4b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45a4b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="45a4b-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="45a4b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="45a4b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45a4b-130">See also</span></span>



- [<span data-ttu-id="45a4b-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="45a4b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

