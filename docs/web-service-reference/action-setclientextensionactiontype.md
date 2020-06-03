---
title: Action (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Das Action-Element enthält die Aktion, die der Exchange-Server für eine APP ausführen sollte.
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529686"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="a7843-103">Action (SetClientExtensionActionType)</span><span class="sxs-lookup"><span data-stu-id="a7843-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="a7843-104">Das **Action** -Element enthält die Aktion, die der Exchange-Server für eine APP ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="a7843-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="a7843-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="a7843-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7843-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7843-106">Attributes and elements</span></span>

<span data-ttu-id="a7843-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7843-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7843-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7843-108">Attributes</span></span>

|<span data-ttu-id="a7843-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a7843-109">**Attribute**</span></span>|<span data-ttu-id="a7843-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7843-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7843-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="a7843-111">ActionId</span></span>  <br/> |<span data-ttu-id="a7843-112">Gibt den Bezeichner der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="a7843-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="a7843-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7843-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a7843-114">ExtensionID geändert</span><span class="sxs-lookup"><span data-stu-id="a7843-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="a7843-115">Gibt den Bezeichner der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a7843-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="a7843-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7843-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="a7843-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="a7843-117">ActionId</span></span>

|<span data-ttu-id="a7843-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7843-118">**Value**</span></span>|<span data-ttu-id="a7843-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7843-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7843-120">Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a7843-120">Configure</span></span>  <br/> |<span data-ttu-id="a7843-121">Gibt eine Konfigurationsaktion an.</span><span class="sxs-lookup"><span data-stu-id="a7843-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="a7843-122">Installieren</span><span class="sxs-lookup"><span data-stu-id="a7843-122">Install</span></span>  <br/> |<span data-ttu-id="a7843-123">Gibt eine Installationsaktion an.</span><span class="sxs-lookup"><span data-stu-id="a7843-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="a7843-124">Uninstall</span><span class="sxs-lookup"><span data-stu-id="a7843-124">Uninstall</span></span>  <br/> |<span data-ttu-id="a7843-125">Gibt eine Deinstallations Aktion an.</span><span class="sxs-lookup"><span data-stu-id="a7843-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7843-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7843-126">Child elements</span></span>

|<span data-ttu-id="a7843-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7843-127">**Element**</span></span>|<span data-ttu-id="a7843-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7843-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7843-129">Client Extension</span><span class="sxs-lookup"><span data-stu-id="a7843-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="a7843-130">Enthält Benutzer-und Konfigurationsinformationen zu einer App.</span><span class="sxs-lookup"><span data-stu-id="a7843-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7843-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7843-131">Parent elements</span></span>

|<span data-ttu-id="a7843-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7843-132">**Element**</span></span>|<span data-ttu-id="a7843-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7843-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7843-134">Actions (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="a7843-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="a7843-135">Gibt ein Array von **Action** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="a7843-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7843-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7843-136">Remarks</span></span>

<span data-ttu-id="a7843-137">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a7843-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a7843-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a7843-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7843-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a7843-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7843-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7843-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7843-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7843-141">Schema Name</span></span>  <br/> |<span data-ttu-id="a7843-142">Typschema</span><span class="sxs-lookup"><span data-stu-id="a7843-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="a7843-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7843-143">Validation File</span></span>  <br/> |<span data-ttu-id="a7843-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a7843-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7843-145">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a7843-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a7843-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7843-146">See also</span></span>

- [<span data-ttu-id="a7843-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a7843-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

