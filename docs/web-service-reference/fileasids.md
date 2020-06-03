---
title: FileAsIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 71cae100-b68e-454b-b9b6-ddbcb4d78f3f
description: Das FileAsIds-Element gibt ein Array von StringAttributedValue-Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: ecdf30fac345834600439227709504b0d56b988b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461044"
---
# <a name="fileasids"></a><span data-ttu-id="1ab4e-103">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="1ab4e-103">FileAsIds</span></span>

<span data-ttu-id="1ab4e-104">Das **FileAsIds** -Element gibt ein Array von **StringAttributedValue** -Elementen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-104">The **FileAsIds** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<FileAsIds>
    <StringAttributedValue/>
<FileAsIds>
```

 <span data-ttu-id="1ab4e-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="1ab4e-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ab4e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab4e-106">Attributes and elements</span></span>

<span data-ttu-id="1ab4e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ab4e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ab4e-108">Attributes</span></span>

<span data-ttu-id="1ab4e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ab4e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab4e-110">Child elements</span></span>

|<span data-ttu-id="1ab4e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ab4e-111">**Element**</span></span>|<span data-ttu-id="1ab4e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ab4e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ab4e-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1ab4e-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="1ab4e-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ab4e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab4e-115">Parent elements</span></span>

|<span data-ttu-id="1ab4e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ab4e-116">**Element**</span></span>|<span data-ttu-id="1ab4e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ab4e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ab4e-118">Persona</span><span class="sxs-lookup"><span data-stu-id="1ab4e-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="1ab4e-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ab4e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ab4e-120">Remarks</span></span>

<span data-ttu-id="1ab4e-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1ab4e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1ab4e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ab4e-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1ab4e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ab4e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ab4e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ab4e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ab4e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1ab4e-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1ab4e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1ab4e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ab4e-127">Validation File</span></span>  <br/> |<span data-ttu-id="1ab4e-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1ab4e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ab4e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1ab4e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1ab4e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab4e-130">See also</span></span>



- [<span data-ttu-id="1ab4e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ab4e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

