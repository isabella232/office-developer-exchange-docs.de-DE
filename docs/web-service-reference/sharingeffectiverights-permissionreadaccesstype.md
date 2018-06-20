---
title: SharingEffectiveRights (PermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: Das SharingEffectiveRights-Element gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird.
ms.openlocfilehash: 19e67827dd2dbff6fb70423980d670da5cc257a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831486"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="118a8-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="118a8-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="118a8-104">Das **SharingEffectiveRights** -Element gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="118a8-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="118a8-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="118a8-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="118a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="118a8-106">Attributes and elements</span></span>

<span data-ttu-id="118a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="118a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="118a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="118a8-108">Attributes</span></span>

<span data-ttu-id="118a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="118a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="118a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="118a8-110">Child elements</span></span>

<span data-ttu-id="118a8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="118a8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="118a8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="118a8-112">Parent elements</span></span>

|<span data-ttu-id="118a8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="118a8-113">**Element**</span></span>|<span data-ttu-id="118a8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="118a8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="118a8-115">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="118a8-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="118a8-116">Stellt einen Kontakteordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="118a8-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="118a8-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="118a8-117">Text value</span></span>

<span data-ttu-id="118a8-118">Die folgende Tabelle enthält die möglichen Werte für das **SharingEffectiveRights** -Element.</span><span class="sxs-lookup"><span data-stu-id="118a8-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="118a8-119">**Text-Elementwerte SharingEffectiveRights**</span><span class="sxs-lookup"><span data-stu-id="118a8-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="118a8-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="118a8-120">**Value**</span></span>|<span data-ttu-id="118a8-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="118a8-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="118a8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="118a8-122">None</span></span>  <br/> |<span data-ttu-id="118a8-123">Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen in den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="118a8-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="118a8-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="118a8-124">FullDetails</span></span>  <br/> |<span data-ttu-id="118a8-125">Gibt an, dass der Benutzer die Berechtigung zum Lesen aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="118a8-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="118a8-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="118a8-126">Remarks</span></span>

<span data-ttu-id="118a8-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="118a8-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="118a8-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="118a8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="118a8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="118a8-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="118a8-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="118a8-130">Schema Name</span></span>  <br/> |<span data-ttu-id="118a8-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="118a8-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="118a8-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="118a8-132">Validation File</span></span>  <br/> |<span data-ttu-id="118a8-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="118a8-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="118a8-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="118a8-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="118a8-135">False</span><span class="sxs-lookup"><span data-stu-id="118a8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="118a8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="118a8-136">See also</span></span>



- [<span data-ttu-id="118a8-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="118a8-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

