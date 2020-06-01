---
title: Attribution (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Das Attribution-Element gibt eine Instanz in einem Array von Attributen für ein personatype-Element an.
ms.openlocfilehash: 05b0d41c116f2ed7b8dbb3ac44108bb879256b5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464175"
---
# <a name="attribution-personaattributiontype"></a><span data-ttu-id="9711b-103">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="9711b-103">Attribution (PersonaAttributionType)</span></span>

<span data-ttu-id="9711b-104">Das **Attribution** -Element gibt eine Instanz in einem Array von Attributen für ein **personatype** -Element an.</span><span class="sxs-lookup"><span data-stu-id="9711b-104">The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element.</span></span> 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 <span data-ttu-id="9711b-105">**PersonaAttributionType**</span><span class="sxs-lookup"><span data-stu-id="9711b-105">**PersonaAttributionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9711b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9711b-106">Attributes and elements</span></span>

<span data-ttu-id="9711b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9711b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9711b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9711b-108">Attributes</span></span>

<span data-ttu-id="9711b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9711b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9711b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9711b-110">Child elements</span></span>

|<span data-ttu-id="9711b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9711b-111">**Element**</span></span>|<span data-ttu-id="9711b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9711b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9711b-113">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="9711b-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="9711b-114">Gibt eine Zeichenfolge an, die eine APP oder eine Attribution in einer Persona eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9711b-114">Specifies a string that uniquely identifies an app or an attribution in a persona.</span></span>  <br/> |
|[<span data-ttu-id="9711b-115">SourceId</span><span class="sxs-lookup"><span data-stu-id="9711b-115">SourceId</span></span>](sourceid.md) <br/> |<span data-ttu-id="9711b-116">Gibt den Bezeichner des Kontakts oder Active Directory Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="9711b-116">Specifies the identifier of the contact or Active Directory recipient.</span></span>  <br/> |
|[<span data-ttu-id="9711b-117">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="9711b-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="9711b-118">Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreter Benutzers oder einer Regel.</span><span class="sxs-lookup"><span data-stu-id="9711b-118">Defines the display name of a folder, contact, distribution list, delegate user, or rule.</span></span>  <br/> |
|[<span data-ttu-id="9711b-119">Isschreibbar</span><span class="sxs-lookup"><span data-stu-id="9711b-119">IsWritable</span></span>](iswritable.md) <br/> |<span data-ttu-id="9711b-120">Gibt an, ob der zugrunde liegende Kontakt oder Active Directory Empfänger in geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9711b-120">Specifies whether the underlying contact or Active Directory recipient can be written to.</span></span>  <br/> |
|[<span data-ttu-id="9711b-121">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="9711b-121">IsQuickContact</span></span>](isquickcontact.md) <br/> |<span data-ttu-id="9711b-122">Gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt oder Active Directory Empfänger ein schnell Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="9711b-122">Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.</span></span>  <br/> |
|[<span data-ttu-id="9711b-123">IsHidden</span><span class="sxs-lookup"><span data-stu-id="9711b-123">IsHidden</span></span>](ishidden.md) <br/> |<span data-ttu-id="9711b-124">Enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt oder Active Directory Empfänger ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9711b-124">Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.</span></span>  <br/> |
|[<span data-ttu-id="9711b-125">FolderId</span><span class="sxs-lookup"><span data-stu-id="9711b-125">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="9711b-126">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="9711b-126">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9711b-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9711b-127">Parent elements</span></span>

|<span data-ttu-id="9711b-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="9711b-128">**Element**</span></span>|<span data-ttu-id="9711b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9711b-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9711b-130">Zuordnungen (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="9711b-130">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="9711b-131">Gibt ein Array mit Zuordnungsinformationen für einen oder mehrere der Kontakte oder Active Directory-Empfänger (AD) an, die in der zugeordneten Rolle aggregiert sind.</span><span class="sxs-lookup"><span data-stu-id="9711b-131">Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9711b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9711b-132">Remarks</span></span>

<span data-ttu-id="9711b-133">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9711b-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9711b-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9711b-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9711b-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9711b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9711b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="9711b-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9711b-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9711b-137">Schema Name</span></span>  <br/> |<span data-ttu-id="9711b-138">Typschema</span><span class="sxs-lookup"><span data-stu-id="9711b-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="9711b-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9711b-139">Validation File</span></span>  <br/> |<span data-ttu-id="9711b-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9711b-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9711b-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9711b-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9711b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9711b-142">See also</span></span>

- [<span data-ttu-id="9711b-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9711b-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

