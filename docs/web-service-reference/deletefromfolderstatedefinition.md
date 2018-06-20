---
title: DeleteFromFolderStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3aba59a0-f12a-48b5-842b-11cf4530dd51
description: Das DeleteFromFolderStateDefinition-Element gibt den Status auf, wenn ein Element aus einem Ordner gelöscht wird.
ms.openlocfilehash: 7b6374b9fa55d3b08569e8ac9e247dd6e5bebc24
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757923"
---
# <a name="deletefromfolderstatedefinition"></a><span data-ttu-id="66c48-103">DeleteFromFolderStateDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-103">DeleteFromFolderStateDefinition</span></span>

<span data-ttu-id="66c48-104">Das **DeleteFromFolderStateDefinition** -Element gibt den Status auf, wenn ein Element aus einem Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="66c48-104">The **DeleteFromFolderStateDefinition** element specifies the state when an item is deleted from a folder.</span></span> 
  
```XML
<DeleteFromFolderStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeleteFromFolderStateDefinition>
```

 <span data-ttu-id="66c48-105">**DeleteFromFolderStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="66c48-105">**DeleteFromFolderStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66c48-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66c48-106">Attributes and elements</span></span>

<span data-ttu-id="66c48-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66c48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66c48-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66c48-108">Attributes</span></span>

<span data-ttu-id="66c48-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="66c48-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66c48-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66c48-110">Child elements</span></span>

|<span data-ttu-id="66c48-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="66c48-111">**Element**</span></span>|<span data-ttu-id="66c48-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66c48-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66c48-113">Vorkommen (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="66c48-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="66c48-114">Gibt das Datum des Vorkommens ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="66c48-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="66c48-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="66c48-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="66c48-116">Gibt einen Boolean-Wert, der angibt, ob ein Vorkommen des Kalenderelements vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="66c48-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66c48-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66c48-117">Parent elements</span></span>

|<span data-ttu-id="66c48-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="66c48-118">**Element**</span></span>|<span data-ttu-id="66c48-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66c48-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66c48-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="66c48-121">Gibt eine Definition Zustand.</span><span class="sxs-lookup"><span data-stu-id="66c48-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66c48-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66c48-122">Remarks</span></span>

<span data-ttu-id="66c48-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="66c48-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="66c48-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="66c48-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66c48-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66c48-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66c48-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="66c48-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66c48-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66c48-127">Schema Name</span></span>  <br/> |<span data-ttu-id="66c48-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="66c48-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="66c48-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66c48-129">Validation File</span></span>  <br/> |<span data-ttu-id="66c48-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66c48-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="66c48-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="66c48-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="66c48-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66c48-132">See also</span></span>

- [<span data-ttu-id="66c48-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66c48-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

