---
title: Imaddresses (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b95d0a8b-15a6-4711-b014-55698dbd679c
description: Das imaddresses-Element gibt ein Array von sofortnachrichtenadressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: 6714af5d88e50047f48da2f10dbb33d2e2feb724
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460442"
---
# <a name="imaddresses-arrayofstringattributedvaluestype"></a><span data-ttu-id="e128e-103">Imaddresses (ArrayOfStringAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="e128e-103">ImAddresses (ArrayOfStringAttributedValuesType)</span></span>

<span data-ttu-id="e128e-104">Das **imaddresses** -Element gibt ein Array von sofortnachrichtenadressen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="e128e-104">The **ImAddresses** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses>
    <StringAttributedValue/>
</ImAddresses>
```

 <span data-ttu-id="e128e-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="e128e-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e128e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e128e-106">Attributes and elements</span></span>

<span data-ttu-id="e128e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e128e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e128e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e128e-108">Attributes</span></span>

<span data-ttu-id="e128e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e128e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e128e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e128e-110">Child elements</span></span>

|<span data-ttu-id="e128e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e128e-111">**Element**</span></span>|<span data-ttu-id="e128e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e128e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e128e-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e128e-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="e128e-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e128e-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e128e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e128e-115">Parent elements</span></span>

|<span data-ttu-id="e128e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e128e-116">**Element**</span></span>|<span data-ttu-id="e128e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e128e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e128e-118">Persona</span><span class="sxs-lookup"><span data-stu-id="e128e-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="e128e-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e128e-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e128e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e128e-120">Remarks</span></span>

<span data-ttu-id="e128e-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e128e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e128e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e128e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e128e-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e128e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e128e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e128e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e128e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e128e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e128e-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="e128e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e128e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e128e-127">Validation File</span></span>  <br/> |<span data-ttu-id="e128e-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e128e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e128e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e128e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e128e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e128e-130">See also</span></span>



- [<span data-ttu-id="e128e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e128e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

