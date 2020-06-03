---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: Das BusinessAddresses-Element gibt ein Array von Geschäftsadressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: d314d0de679f8eabc51dc9ee3b2e9a57cd0b8da1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465926"
---
# <a name="businessaddresses"></a><span data-ttu-id="2c222-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="2c222-103">BusinessAddresses</span></span>

<span data-ttu-id="2c222-104">Das **BusinessAddresses** -Element gibt ein Array von Geschäftsadressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="2c222-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="2c222-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2c222-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c222-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c222-106">Attributes and elements</span></span>

<span data-ttu-id="2c222-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c222-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c222-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c222-108">Attributes</span></span>

<span data-ttu-id="2c222-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c222-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c222-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c222-110">Child elements</span></span>

|<span data-ttu-id="2c222-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c222-111">**Element**</span></span>|<span data-ttu-id="2c222-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c222-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c222-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2c222-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="2c222-114">Gibt eine Instanz eines Arrays von Postadressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="2c222-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c222-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c222-115">Parent elements</span></span>

|<span data-ttu-id="2c222-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c222-116">**Element**</span></span>|<span data-ttu-id="2c222-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c222-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c222-118">Persona</span><span class="sxs-lookup"><span data-stu-id="2c222-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2c222-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c222-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c222-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c222-120">Remarks</span></span>

<span data-ttu-id="2c222-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2c222-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2c222-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2c222-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c222-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2c222-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c222-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c222-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c222-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c222-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2c222-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="2c222-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2c222-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c222-127">Validation File</span></span>  <br/> |<span data-ttu-id="2c222-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2c222-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c222-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2c222-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2c222-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c222-130">See also</span></span>



- [<span data-ttu-id="2c222-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c222-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

