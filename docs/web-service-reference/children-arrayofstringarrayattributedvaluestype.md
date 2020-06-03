---
title: Untergeordnete Elemente (ArrayOfStringArrayAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: Das Children-Element gibt ein Array von untergeordneten Namen und Bezeichnern der Quell Zuordnungen für die zugeordnete persona an.
ms.openlocfilehash: f4217f8a444bfdb6d86ff7b912294cfad9cbdcdc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460232"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a><span data-ttu-id="283f6-103">Untergeordnete Elemente (ArrayOfStringArrayAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="283f6-103">Children (ArrayOfStringArrayAttributedValuesType)</span></span>

<span data-ttu-id="283f6-104">Das **Children** -Element gibt ein Array von untergeordneten Namen und Bezeichnern der Quell Zuordnungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="283f6-104">The **Children** element specifies an array of child names and identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 <span data-ttu-id="283f6-105">**ArrayOfStringArrayAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="283f6-105">**ArrayOfStringArrayAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="283f6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="283f6-106">Attributes and elements</span></span>

<span data-ttu-id="283f6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="283f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="283f6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="283f6-108">Attributes</span></span>

<span data-ttu-id="283f6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="283f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="283f6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="283f6-110">Child elements</span></span>

|<span data-ttu-id="283f6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="283f6-111">**Element**</span></span>|<span data-ttu-id="283f6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="283f6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="283f6-113">StringArrayAttributedValue</span><span class="sxs-lookup"><span data-stu-id="283f6-113">StringArrayAttributedValue</span></span>](stringarrayattributedvalue.md) <br/> |<span data-ttu-id="283f6-114">Gibt eine Instanz eines Arrays von Zeichenfolgendaten für ein Persona-Element an.</span><span class="sxs-lookup"><span data-stu-id="283f6-114">Specifies an instance of an array of string data for a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="283f6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="283f6-115">Parent elements</span></span>

|<span data-ttu-id="283f6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="283f6-116">**Element**</span></span>|<span data-ttu-id="283f6-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="283f6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="283f6-118">Persona</span><span class="sxs-lookup"><span data-stu-id="283f6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="283f6-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="283f6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="283f6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="283f6-120">Remarks</span></span>

<span data-ttu-id="283f6-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="283f6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="283f6-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="283f6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="283f6-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="283f6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="283f6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="283f6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="283f6-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="283f6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="283f6-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="283f6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="283f6-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="283f6-127">Validation File</span></span>  <br/> |<span data-ttu-id="283f6-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="283f6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="283f6-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="283f6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="283f6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="283f6-130">See also</span></span>



- [<span data-ttu-id="283f6-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="283f6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

