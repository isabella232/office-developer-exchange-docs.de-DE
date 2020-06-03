---
title: GivenNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 64d86c24-07b8-448d-ad37-47f104777df3
description: Das GivenNames-Element gibt ein Array mit angegebenen Namenswerten und die Bezeichner der Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: c76d69344b59fb56377a13b9ea4a588acc382013
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530127"
---
# <a name="givennames"></a><span data-ttu-id="d873c-103">GivenNames</span><span class="sxs-lookup"><span data-stu-id="d873c-103">GivenNames</span></span>

<span data-ttu-id="d873c-104">Das **GivenNames** -Element gibt ein Array mit angegebenen Namenswerten und die Bezeichner der Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="d873c-104">The **GivenNames** element specifies an array of given name values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```xml
<GivenNames>
    <StringAttributedValue/>
</GivenNames>
```

 <span data-ttu-id="d873c-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="d873c-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d873c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d873c-106">Attributes and elements</span></span>

<span data-ttu-id="d873c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d873c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d873c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d873c-108">Attributes</span></span>

<span data-ttu-id="d873c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d873c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d873c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d873c-110">Child elements</span></span>

|<span data-ttu-id="d873c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d873c-111">**Element**</span></span>|<span data-ttu-id="d873c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d873c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d873c-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d873c-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="d873c-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d873c-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d873c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d873c-115">Parent elements</span></span>

|<span data-ttu-id="d873c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d873c-116">**Element**</span></span>|<span data-ttu-id="d873c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d873c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d873c-118">Persona</span><span class="sxs-lookup"><span data-stu-id="d873c-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="d873c-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d873c-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d873c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d873c-120">Remarks</span></span>

<span data-ttu-id="d873c-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d873c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d873c-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d873c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d873c-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d873c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d873c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d873c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d873c-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d873c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d873c-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="d873c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d873c-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d873c-127">Validation File</span></span>  <br/> |<span data-ttu-id="d873c-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d873c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d873c-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d873c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d873c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d873c-130">See also</span></span>



- [<span data-ttu-id="d873c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d873c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

