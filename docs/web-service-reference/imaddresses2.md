---
title: ImAddresses2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 328f29b9-3a9c-4d9a-a85f-5ffff84e266a
description: Das ImAddresses2-Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: f61084f22eb9d38766c45e63dfbacc0882ccaaca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829870"
---
# <a name="imaddresses2"></a><span data-ttu-id="87589-103">ImAddresses2</span><span class="sxs-lookup"><span data-stu-id="87589-103">ImAddresses2</span></span>

<span data-ttu-id="87589-104">Das **ImAddresses2** -Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="87589-104">The **ImAddresses2** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses2>
    <StringAttributedValue/>
</ImAddresses2>
```

 <span data-ttu-id="87589-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="87589-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87589-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="87589-106">Attributes and elements</span></span>

<span data-ttu-id="87589-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="87589-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87589-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="87589-108">Attributes</span></span>

<span data-ttu-id="87589-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="87589-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87589-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87589-110">Child elements</span></span>

|<span data-ttu-id="87589-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="87589-111">**Element**</span></span>|<span data-ttu-id="87589-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87589-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87589-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="87589-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="87589-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87589-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="87589-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87589-115">Parent elements</span></span>

|<span data-ttu-id="87589-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="87589-116">**Element**</span></span>|<span data-ttu-id="87589-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87589-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87589-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="87589-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="87589-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87589-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87589-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87589-120">Remarks</span></span>

<span data-ttu-id="87589-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="87589-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="87589-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="87589-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87589-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="87589-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87589-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="87589-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87589-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="87589-125">Schema Name</span></span>  <br/> |<span data-ttu-id="87589-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="87589-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="87589-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="87589-127">Validation File</span></span>  <br/> |<span data-ttu-id="87589-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87589-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="87589-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="87589-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="87589-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87589-130">See also</span></span>



- [<span data-ttu-id="87589-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="87589-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

