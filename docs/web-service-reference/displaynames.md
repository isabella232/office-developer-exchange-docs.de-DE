---
title: Display Names
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dedd43c8-c1d6-4671-89c5-ce7ab3979fda
description: Das Display Names-Element gibt ein Array von Anzeigenamen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: 7d0c528b5b7f9adae271a42380550115fbcf94d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460736"
---
# <a name="displaynames"></a><span data-ttu-id="15561-103">Display Names</span><span class="sxs-lookup"><span data-stu-id="15561-103">DisplayNames</span></span>

<span data-ttu-id="15561-104">Das **Display Names** -Element gibt ein Array von Anzeigenamen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="15561-104">The **DisplayNames** element specifies an array of display names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```xml
<DisplayNames>
    <StringAttributedValue></StringAttributedValue>
</DisplayNames>
```

 <span data-ttu-id="15561-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="15561-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15561-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="15561-106">Attributes and elements</span></span>

<span data-ttu-id="15561-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="15561-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15561-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="15561-108">Attributes</span></span>

<span data-ttu-id="15561-109">Keine</span><span class="sxs-lookup"><span data-stu-id="15561-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15561-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15561-110">Child elements</span></span>

|<span data-ttu-id="15561-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="15561-111">**Element**</span></span>|<span data-ttu-id="15561-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15561-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15561-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="15561-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="15561-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="15561-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15561-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15561-115">Parent elements</span></span>

|<span data-ttu-id="15561-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="15561-116">**Element**</span></span>|<span data-ttu-id="15561-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15561-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15561-118">Persona</span><span class="sxs-lookup"><span data-stu-id="15561-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="15561-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15561-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15561-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15561-120">Remarks</span></span>

<span data-ttu-id="15561-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="15561-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="15561-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="15561-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15561-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="15561-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15561-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="15561-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15561-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="15561-125">Schema Name</span></span>  <br/> |<span data-ttu-id="15561-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="15561-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="15561-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="15561-127">Validation File</span></span>  <br/> |<span data-ttu-id="15561-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="15561-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="15561-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="15561-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="15561-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15561-130">See also</span></span>

- [<span data-ttu-id="15561-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="15561-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

