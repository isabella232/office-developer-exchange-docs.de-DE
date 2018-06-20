---
title: ImAddresses3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cab51a28-dfad-4c70-aafe-e239321b784e
description: Das ImAddresses3-Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 1d6ebf9d8e831f36ea7d947a72c60c58fa5b1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829874"
---
# <a name="imaddresses3"></a><span data-ttu-id="1864f-103">ImAddresses3</span><span class="sxs-lookup"><span data-stu-id="1864f-103">ImAddresses3</span></span>

<span data-ttu-id="1864f-104">Das **ImAddresses3** -Element gibt ein Array von instant Messaging-Adressen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="1864f-104">The **ImAddresses3** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses3>
    <StringAttributedValue/>
</ImAddresses3>
```

 <span data-ttu-id="1864f-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="1864f-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1864f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1864f-106">Attributes and elements</span></span>

<span data-ttu-id="1864f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1864f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1864f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1864f-108">Attributes</span></span>

<span data-ttu-id="1864f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1864f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1864f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1864f-110">Child elements</span></span>

|<span data-ttu-id="1864f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1864f-111">**Element**</span></span>|<span data-ttu-id="1864f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1864f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1864f-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1864f-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="1864f-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1864f-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1864f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1864f-115">Parent elements</span></span>

|<span data-ttu-id="1864f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1864f-116">**Element**</span></span>|<span data-ttu-id="1864f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1864f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1864f-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="1864f-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="1864f-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1864f-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1864f-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1864f-120">Remarks</span></span>

<span data-ttu-id="1864f-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1864f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1864f-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1864f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1864f-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1864f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1864f-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1864f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1864f-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1864f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1864f-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1864f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1864f-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1864f-127">Validation File</span></span>  <br/> |<span data-ttu-id="1864f-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1864f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1864f-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1864f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1864f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1864f-130">See also</span></span>



- [<span data-ttu-id="1864f-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1864f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

