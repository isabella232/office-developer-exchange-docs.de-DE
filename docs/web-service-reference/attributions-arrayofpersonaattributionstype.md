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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460323"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="80c54-103">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="80c54-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="80c54-104">Das **Attributes** -Element gibt ein Array von Zuordnungsinformationen für einen oder mehrere Kontakte oder Active Directory Empfänger an, die in der zugeordneten Rolle aggregiert sind.</span><span class="sxs-lookup"><span data-stu-id="80c54-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="80c54-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="80c54-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80c54-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="80c54-106">Attributes and elements</span></span>

<span data-ttu-id="80c54-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="80c54-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80c54-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="80c54-108">Attributes</span></span>

<span data-ttu-id="80c54-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="80c54-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80c54-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80c54-110">Child elements</span></span>

|<span data-ttu-id="80c54-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="80c54-111">**Element**</span></span>|<span data-ttu-id="80c54-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80c54-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80c54-113">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="80c54-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="80c54-114">Gibt eine Instanz in einem Array von Attributen für ein **personatype** -Element an.</span><span class="sxs-lookup"><span data-stu-id="80c54-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80c54-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80c54-115">Parent elements</span></span>

|<span data-ttu-id="80c54-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="80c54-116">**Element**</span></span>|<span data-ttu-id="80c54-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80c54-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80c54-118">Persona</span><span class="sxs-lookup"><span data-stu-id="80c54-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="80c54-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80c54-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80c54-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80c54-120">Remarks</span></span>

<span data-ttu-id="80c54-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="80c54-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80c54-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="80c54-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80c54-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="80c54-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80c54-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="80c54-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80c54-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="80c54-125">Schema Name</span></span>  <br/> |<span data-ttu-id="80c54-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="80c54-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="80c54-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="80c54-127">Validation File</span></span>  <br/> |<span data-ttu-id="80c54-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="80c54-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="80c54-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="80c54-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="80c54-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c54-130">See also</span></span>

- [<span data-ttu-id="80c54-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="80c54-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

