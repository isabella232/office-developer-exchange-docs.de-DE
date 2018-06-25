---
title: Aktion (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Das Action-Element enthält die Aktion, die der Exchange-Server für eine app ausgeführt werden soll.
ms.openlocfilehash: a231cedfa6e4759dabfcbecfbe9a9b851f834247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757215"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="029c8-103">Aktion (SetClientExtensionActionType)</span><span class="sxs-lookup"><span data-stu-id="029c8-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="029c8-104">Das **Action** -Element enthält die Aktion, die der Exchange-Server für eine app ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="029c8-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="029c8-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="029c8-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="029c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="029c8-106">Attributes and elements</span></span>

<span data-ttu-id="029c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="029c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="029c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="029c8-108">Attributes</span></span>

|<span data-ttu-id="029c8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="029c8-109">**Attribute**</span></span>|<span data-ttu-id="029c8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="029c8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="029c8-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="029c8-111">ActionId</span></span>  <br/> |<span data-ttu-id="029c8-112">Gibt den Bezeichner der Aktion.</span><span class="sxs-lookup"><span data-stu-id="029c8-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="029c8-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="029c8-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="029c8-114">ExtensionID geändert</span><span class="sxs-lookup"><span data-stu-id="029c8-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="029c8-115">Gibt den Bezeichner der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="029c8-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="029c8-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="029c8-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="029c8-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="029c8-117">ActionId</span></span>

|<span data-ttu-id="029c8-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="029c8-118">**Value**</span></span>|<span data-ttu-id="029c8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="029c8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="029c8-120">Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="029c8-120">Configure</span></span>  <br/> |<span data-ttu-id="029c8-121">Gibt eine Konfigurationsaktion an.</span><span class="sxs-lookup"><span data-stu-id="029c8-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="029c8-122">Installieren Sie</span><span class="sxs-lookup"><span data-stu-id="029c8-122">Install</span></span>  <br/> |<span data-ttu-id="029c8-123">Gibt eine Installation Aktion an.</span><span class="sxs-lookup"><span data-stu-id="029c8-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="029c8-124">Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="029c8-124">Uninstall</span></span>  <br/> |<span data-ttu-id="029c8-125">Gibt eine Deinstallation Aktion an.</span><span class="sxs-lookup"><span data-stu-id="029c8-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="029c8-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="029c8-126">Child elements</span></span>

|<span data-ttu-id="029c8-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="029c8-127">**Element**</span></span>|<span data-ttu-id="029c8-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="029c8-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="029c8-129">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="029c8-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="029c8-130">Benutzer- und Konfigurationsdaten Informationen zu einer app enthält.</span><span class="sxs-lookup"><span data-stu-id="029c8-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="029c8-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="029c8-131">Parent elements</span></span>

|<span data-ttu-id="029c8-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="029c8-132">**Element**</span></span>|<span data-ttu-id="029c8-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="029c8-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="029c8-134">Aktionen (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="029c8-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="029c8-135">Gibt ein Array von **Action** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="029c8-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="029c8-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="029c8-136">Remarks</span></span>

<span data-ttu-id="029c8-137">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="029c8-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="029c8-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="029c8-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="029c8-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="029c8-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="029c8-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="029c8-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="029c8-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="029c8-141">Schema Name</span></span>  <br/> |<span data-ttu-id="029c8-142">Typschema</span><span class="sxs-lookup"><span data-stu-id="029c8-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="029c8-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="029c8-143">Validation File</span></span>  <br/> |<span data-ttu-id="029c8-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="029c8-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="029c8-145">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="029c8-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="029c8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="029c8-146">See also</span></span>

- [<span data-ttu-id="029c8-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="029c8-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

