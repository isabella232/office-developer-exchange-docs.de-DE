---
title: HomeFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 459ddb1c-8cff-4125-b6fa-dc93c183dee8
description: Das HomeFaxes-Element gibt ein Array von privaten Faxnummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: d49eb9e12547e4011e4ba403cb898c0fe6e9bf02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460848"
---
# <a name="homefaxes"></a><span data-ttu-id="83877-103">HomeFaxes</span><span class="sxs-lookup"><span data-stu-id="83877-103">HomeFaxes</span></span>

<span data-ttu-id="83877-104">Das **HomeFaxes** -Element gibt ein Array von privaten Faxnummern und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="83877-104">The **HomeFaxes** element specifies an array of home fax numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeFaxes>
    <PhoneNumberAttributedValue/>
</HomeFaxes>
```

 <span data-ttu-id="83877-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="83877-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83877-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83877-106">Attributes and elements</span></span>

<span data-ttu-id="83877-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83877-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83877-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83877-108">Attributes</span></span>

<span data-ttu-id="83877-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83877-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83877-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83877-110">Child elements</span></span>

|<span data-ttu-id="83877-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83877-111">**Element**</span></span>|<span data-ttu-id="83877-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83877-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83877-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="83877-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="83877-114">Enthält eine einzelne attributierte Telefonnummer für eine Person.</span><span class="sxs-lookup"><span data-stu-id="83877-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83877-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83877-115">Parent elements</span></span>

|<span data-ttu-id="83877-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="83877-116">**Element**</span></span>|<span data-ttu-id="83877-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83877-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83877-118">Persona</span><span class="sxs-lookup"><span data-stu-id="83877-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="83877-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83877-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83877-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83877-120">Remarks</span></span>

<span data-ttu-id="83877-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="83877-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="83877-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83877-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83877-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="83877-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83877-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="83877-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83877-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83877-125">Schema Name</span></span>  <br/> |<span data-ttu-id="83877-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="83877-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="83877-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83877-127">Validation File</span></span>  <br/> |<span data-ttu-id="83877-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="83877-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="83877-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="83877-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="83877-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83877-130">See also</span></span>



- [<span data-ttu-id="83877-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83877-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

