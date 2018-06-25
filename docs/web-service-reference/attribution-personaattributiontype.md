---
title: Zuweisung (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Zuweisung-Element gibt eine Instanz in ein Array von Attributen für ein PersonaType-Element.
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757407"
---
# <a name="attribution-personaattributiontype"></a><span data-ttu-id="7a0de-103">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="7a0de-103">Attribution (PersonaAttributionType)</span></span>

<span data-ttu-id="7a0de-104">**Zuweisung** -Element gibt eine Instanz in ein Array von Attributen für ein **PersonaType** -Element.</span><span class="sxs-lookup"><span data-stu-id="7a0de-104">The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element.</span></span> 
  
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

 <span data-ttu-id="7a0de-105">**PersonaAttributionType**</span><span class="sxs-lookup"><span data-stu-id="7a0de-105">**PersonaAttributionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a0de-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a0de-106">Attributes and elements</span></span>

<span data-ttu-id="7a0de-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a0de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a0de-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a0de-108">Attributes</span></span>

<span data-ttu-id="7a0de-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a0de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a0de-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a0de-110">Child elements</span></span>

|<span data-ttu-id="7a0de-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a0de-111">**Element**</span></span>|<span data-ttu-id="7a0de-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a0de-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a0de-113">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="7a0de-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="7a0de-114">Gibt eine Zeichenfolge, die eine app oder eines Attributes in einer Rolle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7a0de-114">Specifies a string that uniquely identifies an app or an attribution in a persona.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-115">SourceId</span><span class="sxs-lookup"><span data-stu-id="7a0de-115">SourceId</span></span>](sourceid.md) <br/> |<span data-ttu-id="7a0de-116">Gibt den Bezeichner des Kontakts oder der Active Directory-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="7a0de-116">Specifies the identifier of the contact or Active Directory recipient.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-117">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="7a0de-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="7a0de-118">Der Anzeigename eines Ordners, Kontakt, Verteilerliste, Stellvertretungsbenutzers oder Regel definiert.</span><span class="sxs-lookup"><span data-stu-id="7a0de-118">Defines the display name of a folder, contact, distribution list, delegate user, or rule.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-119">IsWritable</span><span class="sxs-lookup"><span data-stu-id="7a0de-119">IsWritable</span></span>](iswritable.md) <br/> |<span data-ttu-id="7a0de-120">Gibt an, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a0de-120">Specifies whether the underlying contact or Active Directory recipient can be written to.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-121">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="7a0de-121">IsQuickContact</span></span>](isquickcontact.md) <br/> |<span data-ttu-id="7a0de-122">Gibt einen Boolean-Wert, der angibt, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger ein schnelles Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="7a0de-122">Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-123">IsHidden</span><span class="sxs-lookup"><span data-stu-id="7a0de-123">IsHidden</span></span>](ishidden.md) <br/> |<span data-ttu-id="7a0de-124">Enthält einen booleschen Wert, der angibt, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a0de-124">Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.</span></span>  <br/> |
|[<span data-ttu-id="7a0de-125">FolderId</span><span class="sxs-lookup"><span data-stu-id="7a0de-125">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="7a0de-126">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="7a0de-126">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a0de-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a0de-127">Parent elements</span></span>

|<span data-ttu-id="7a0de-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a0de-128">**Element**</span></span>|<span data-ttu-id="7a0de-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a0de-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a0de-130">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="7a0de-130">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="7a0de-131">Gibt ein Array von Informationen für eine oder mehrere Kontakte oder active Directory (AD) Empfänger in der zugeordneten Rolle aggregiert.</span><span class="sxs-lookup"><span data-stu-id="7a0de-131">Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a0de-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a0de-132">Remarks</span></span>

<span data-ttu-id="7a0de-133">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7a0de-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a0de-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a0de-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a0de-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7a0de-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a0de-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a0de-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a0de-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a0de-137">Schema Name</span></span>  <br/> |<span data-ttu-id="7a0de-138">Typschema</span><span class="sxs-lookup"><span data-stu-id="7a0de-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="7a0de-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a0de-139">Validation File</span></span>  <br/> |<span data-ttu-id="7a0de-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a0de-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a0de-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7a0de-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7a0de-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a0de-142">See also</span></span>

- [<span data-ttu-id="7a0de-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a0de-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

