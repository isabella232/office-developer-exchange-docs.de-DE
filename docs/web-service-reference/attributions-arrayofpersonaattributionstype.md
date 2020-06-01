---
title: Zuordnungen (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: Das Attributes-Element gibt ein Array von Zuordnungsinformationen für einen oder mehrere Kontakte oder Active Directory Empfänger an, die in der zugeordneten Rolle aggregiert sind.
ms.openlocfilehash: a9883e06a8adbd5c9d3bc7e1edd28c62418df653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460323"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="00797-103">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="00797-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="00797-104">Das **Attributes** -Element gibt ein Array von Zuordnungsinformationen für einen oder mehrere Kontakte oder Active Directory Empfänger an, die in der zugeordneten Rolle aggregiert sind.</span><span class="sxs-lookup"><span data-stu-id="00797-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="00797-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="00797-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00797-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="00797-106">Attributes and elements</span></span>

<span data-ttu-id="00797-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="00797-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00797-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="00797-108">Attributes</span></span>

<span data-ttu-id="00797-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="00797-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00797-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00797-110">Child elements</span></span>

|<span data-ttu-id="00797-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="00797-111">**Element**</span></span>|<span data-ttu-id="00797-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00797-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00797-113">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="00797-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="00797-114">Gibt eine Instanz in einem Array von Attributen für ein **personatype** -Element an.</span><span class="sxs-lookup"><span data-stu-id="00797-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00797-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00797-115">Parent elements</span></span>

|<span data-ttu-id="00797-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="00797-116">**Element**</span></span>|<span data-ttu-id="00797-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00797-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00797-118">Persona</span><span class="sxs-lookup"><span data-stu-id="00797-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="00797-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00797-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00797-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00797-120">Remarks</span></span>

<span data-ttu-id="00797-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="00797-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="00797-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="00797-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00797-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="00797-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00797-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="00797-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00797-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="00797-125">Schema Name</span></span>  <br/> |<span data-ttu-id="00797-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="00797-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="00797-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="00797-127">Validation File</span></span>  <br/> |<span data-ttu-id="00797-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="00797-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="00797-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="00797-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="00797-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00797-130">See also</span></span>

- [<span data-ttu-id="00797-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="00797-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

