---
title: FileAses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81efc37-bb70-4d52-a614-cec87d1b0f04
description: Das FileAses-Element gibt ein Array von StringAttributedValue-Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: 9d97c2c7210e9ae20326d7327c9de4159d5df5a6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461079"
---
# <a name="fileases"></a><span data-ttu-id="2b538-103">FileAses</span><span class="sxs-lookup"><span data-stu-id="2b538-103">FileAses</span></span>

<span data-ttu-id="2b538-104">Das **FileAses** -Element gibt ein Array von **StringAttributedValue** -Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="2b538-104">The **FileAses** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<FileAses>
    <StringAttributedValue/>
</FileAses>
```

 <span data-ttu-id="2b538-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2b538-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b538-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b538-106">Attributes and elements</span></span>

<span data-ttu-id="2b538-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b538-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b538-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b538-108">Attributes</span></span>

<span data-ttu-id="2b538-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b538-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b538-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b538-110">Child elements</span></span>

|<span data-ttu-id="2b538-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b538-111">**Element**</span></span>|<span data-ttu-id="2b538-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b538-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b538-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2b538-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="2b538-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2b538-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b538-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b538-115">Parent elements</span></span>

|<span data-ttu-id="2b538-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b538-116">**Element**</span></span>|<span data-ttu-id="2b538-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b538-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b538-118">Persona</span><span class="sxs-lookup"><span data-stu-id="2b538-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2b538-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2b538-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b538-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b538-120">Remarks</span></span>

<span data-ttu-id="2b538-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2b538-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2b538-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2b538-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b538-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2b538-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b538-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b538-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b538-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b538-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2b538-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="2b538-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2b538-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b538-127">Validation File</span></span>  <br/> |<span data-ttu-id="2b538-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2b538-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b538-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2b538-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2b538-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b538-130">See also</span></span>



- [<span data-ttu-id="2b538-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2b538-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

