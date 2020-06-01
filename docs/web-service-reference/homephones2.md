---
title: HomePhones2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba9bb159-362d-48e0-889d-823cb46ecebf
description: Das HomePhones2-Element gibt ein Array von HomePhone2-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: 5763b38506655828cd86f6633b462873362e8062
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460820"
---
# <a name="homephones2"></a><span data-ttu-id="15606-103">HomePhones2</span><span class="sxs-lookup"><span data-stu-id="15606-103">HomePhones2</span></span>

<span data-ttu-id="15606-104">Das **HomePhones2** -Element gibt ein Array von **HomePhone2** -Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="15606-104">The **HomePhones2** element specifies an array of **HomePhone2** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomePhones2>
    <PhoneNumberAttributedValue/>
</HomePhones2>
```

 <span data-ttu-id="15606-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="15606-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15606-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="15606-106">Attributes and elements</span></span>

<span data-ttu-id="15606-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="15606-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15606-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="15606-108">Attributes</span></span>

<span data-ttu-id="15606-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="15606-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15606-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15606-110">Child elements</span></span>

|<span data-ttu-id="15606-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="15606-111">**Element**</span></span>|<span data-ttu-id="15606-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15606-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15606-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="15606-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="15606-114">Enthält eine einzelne attributierte Telefonnummer für eine Person.</span><span class="sxs-lookup"><span data-stu-id="15606-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15606-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15606-115">Parent elements</span></span>

|<span data-ttu-id="15606-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="15606-116">**Element**</span></span>|<span data-ttu-id="15606-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15606-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15606-118">Persona</span><span class="sxs-lookup"><span data-stu-id="15606-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="15606-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15606-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15606-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15606-120">Remarks</span></span>

<span data-ttu-id="15606-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="15606-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="15606-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="15606-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15606-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="15606-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15606-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="15606-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15606-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="15606-125">Schema Name</span></span>  <br/> |<span data-ttu-id="15606-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="15606-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="15606-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="15606-127">Validation File</span></span>  <br/> |<span data-ttu-id="15606-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="15606-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="15606-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="15606-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="15606-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15606-130">See also</span></span>



- [<span data-ttu-id="15606-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="15606-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

