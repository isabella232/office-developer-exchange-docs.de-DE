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
description: Das SharingEffectiveRights-Element gibt die Berechtigungen an, die der Benutzer für die Kontaktdaten verwendet, die freigegeben werden.
ms.openlocfilehash: 64b1e6d831068e9699e9cd47693e74919e0416a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526662"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="5a3ef-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="5a3ef-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="5a3ef-104">Das **SharingEffectiveRights** -Element gibt die Berechtigungen an, die der Benutzer für die Kontaktdaten verwendet, die freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="5a3ef-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a3ef-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a3ef-106">Attributes and elements</span></span>

<span data-ttu-id="5a3ef-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a3ef-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a3ef-108">Attributes</span></span>

<span data-ttu-id="5a3ef-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a3ef-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a3ef-110">Child elements</span></span>

<span data-ttu-id="5a3ef-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a3ef-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a3ef-112">Parent elements</span></span>

|<span data-ttu-id="5a3ef-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-113">**Element**</span></span>|<span data-ttu-id="5a3ef-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a3ef-115">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="5a3ef-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="5a3ef-116">Stellt einen Kontakteordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a3ef-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5a3ef-117">Text value</span></span>

<span data-ttu-id="5a3ef-118">In der folgenden Tabelle sind die möglichen Werte für das **SharingEffectiveRights** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="5a3ef-119">**SharingEffectiveRights-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="5a3ef-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-120">**Value**</span></span>|<span data-ttu-id="5a3ef-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a3ef-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a3ef-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5a3ef-122">None</span></span>  <br/> |<span data-ttu-id="5a3ef-123">Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="5a3ef-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="5a3ef-124">FullDetails</span></span>  <br/> |<span data-ttu-id="5a3ef-125">Gibt an, dass der Benutzer über die Berechtigung zum Lesen aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a3ef-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a3ef-126">Remarks</span></span>

<span data-ttu-id="5a3ef-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a3ef-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5a3ef-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a3ef-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a3ef-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a3ef-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a3ef-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5a3ef-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5a3ef-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a3ef-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a3ef-132">Validation File</span></span>  <br/> |<span data-ttu-id="5a3ef-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a3ef-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a3ef-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a3ef-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a3ef-135">False</span><span class="sxs-lookup"><span data-stu-id="5a3ef-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a3ef-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a3ef-136">See also</span></span>



- [<span data-ttu-id="5a3ef-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5a3ef-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

