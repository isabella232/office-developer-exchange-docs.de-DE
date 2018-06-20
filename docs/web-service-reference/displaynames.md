---
title: DisplayNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dedd43c8-c1d6-4671-89c5-ce7ab3979fda
description: Die DisplayNames, den-Element gibt ein Array von an anzeigen Namen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 66f10edd26a467af290535196778fbcb550c16ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758069"
---
# <a name="displaynames"></a><span data-ttu-id="66985-103">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="66985-103">DisplayNames</span></span>

<span data-ttu-id="66985-104">Das **DisplayNames** -Element gibt ein Array von Anzeigenamen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="66985-104">The **DisplayNames** element specifies an array of display names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```xml
<DisplayNames>
    <StringAttributedValue></StringAttributedValue>
</DisplayNames>
```

 <span data-ttu-id="66985-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="66985-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66985-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66985-106">Attributes and elements</span></span>

<span data-ttu-id="66985-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66985-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66985-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66985-108">Attributes</span></span>

<span data-ttu-id="66985-109">Keine</span><span class="sxs-lookup"><span data-stu-id="66985-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66985-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66985-110">Child elements</span></span>

|<span data-ttu-id="66985-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="66985-111">**Element**</span></span>|<span data-ttu-id="66985-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66985-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66985-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="66985-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="66985-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="66985-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66985-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66985-115">Parent elements</span></span>

|<span data-ttu-id="66985-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="66985-116">**Element**</span></span>|<span data-ttu-id="66985-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66985-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66985-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="66985-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="66985-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66985-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66985-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66985-120">Remarks</span></span>

<span data-ttu-id="66985-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="66985-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="66985-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="66985-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66985-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66985-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66985-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="66985-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66985-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66985-125">Schema Name</span></span>  <br/> |<span data-ttu-id="66985-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="66985-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="66985-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66985-127">Validation File</span></span>  <br/> |<span data-ttu-id="66985-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66985-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="66985-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="66985-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="66985-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66985-130">See also</span></span>

- [<span data-ttu-id="66985-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66985-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

