---
title: Hinweise (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: Das Element Marken gibt ein Array von Informationen für eine oder mehrere Kontakte oder Active Directory-Empfänger in der zugeordneten Rolle aggregiert.
ms.openlocfilehash: 52fecb4e4381d5e9dbbaf7134fa18068ba15f6ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757406"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="d24aa-103">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="d24aa-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="d24aa-104">Das Element **Marken** gibt ein Array von Informationen für eine oder mehrere Kontakte oder Active Directory-Empfänger in der zugeordneten Rolle aggregiert.</span><span class="sxs-lookup"><span data-stu-id="d24aa-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="d24aa-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="d24aa-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d24aa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d24aa-106">Attributes and elements</span></span>

<span data-ttu-id="d24aa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d24aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d24aa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d24aa-108">Attributes</span></span>

<span data-ttu-id="d24aa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d24aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d24aa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d24aa-110">Child elements</span></span>

|<span data-ttu-id="d24aa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d24aa-111">**Element**</span></span>|<span data-ttu-id="d24aa-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d24aa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d24aa-113">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d24aa-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="d24aa-114">Gibt eine Instanz in ein Array von Attributen für ein **PersonaType** -Element.</span><span class="sxs-lookup"><span data-stu-id="d24aa-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d24aa-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d24aa-115">Parent elements</span></span>

|<span data-ttu-id="d24aa-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d24aa-116">**Element**</span></span>|<span data-ttu-id="d24aa-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d24aa-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d24aa-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="d24aa-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="d24aa-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d24aa-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d24aa-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d24aa-120">Remarks</span></span>

<span data-ttu-id="d24aa-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d24aa-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d24aa-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d24aa-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d24aa-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d24aa-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d24aa-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d24aa-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d24aa-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d24aa-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d24aa-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="d24aa-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d24aa-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d24aa-127">Validation File</span></span>  <br/> |<span data-ttu-id="d24aa-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d24aa-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d24aa-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d24aa-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d24aa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d24aa-130">See also</span></span>

- [<span data-ttu-id="d24aa-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d24aa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

