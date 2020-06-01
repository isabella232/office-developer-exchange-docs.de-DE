---
title: Hobbys
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f771b066-e42e-4880-bf18-709ad033d2af
description: Das Hobbies-Element gibt ein Array von Hobbies und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: c76f4fc0463928814c61b8d1fb63e4255d6be63d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460953"
---
# <a name="hobbies"></a><span data-ttu-id="aa5b4-103">Hobbys</span><span class="sxs-lookup"><span data-stu-id="aa5b4-103">Hobbies</span></span>

<span data-ttu-id="aa5b4-104">Das **Hobbies** -Element gibt ein Array von Hobbies und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-104">The **Hobbies** element specifies an array of hobbies and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Hobbies>
    <StringAttributedValue/>
</Hobbies>
```

 <span data-ttu-id="aa5b4-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa5b4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aa5b4-106">Attributes and elements</span></span>

<span data-ttu-id="aa5b4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa5b4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa5b4-108">Attributes</span></span>

<span data-ttu-id="aa5b4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa5b4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa5b4-110">Child elements</span></span>

|<span data-ttu-id="aa5b4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-111">**Element**</span></span>|<span data-ttu-id="aa5b4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa5b4-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="aa5b4-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="aa5b4-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa5b4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa5b4-115">Parent elements</span></span>

|<span data-ttu-id="aa5b4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-116">**Element**</span></span>|<span data-ttu-id="aa5b4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa5b4-118">Persona</span><span class="sxs-lookup"><span data-stu-id="aa5b4-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="aa5b4-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa5b4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa5b4-120">Remarks</span></span>

<span data-ttu-id="aa5b4-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aa5b4-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa5b4-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="aa5b4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa5b4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa5b4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa5b4-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aa5b4-125">Schema Name</span></span>  <br/> |<span data-ttu-id="aa5b4-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="aa5b4-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="aa5b4-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aa5b4-127">Validation File</span></span>  <br/> |<span data-ttu-id="aa5b4-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aa5b4-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa5b4-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="aa5b4-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aa5b4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa5b4-130">See also</span></span>



- [<span data-ttu-id="aa5b4-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="aa5b4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

