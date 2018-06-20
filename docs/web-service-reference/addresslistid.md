---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: Das AddressListId-Element gibt den Bezeichner der einer Adressliste.
ms.openlocfilehash: d8a513559b7d127559537b43d7c6c0a4db121702
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757243"
---
# <a name="addresslistid"></a><span data-ttu-id="3d967-103">AddressListId</span><span class="sxs-lookup"><span data-stu-id="3d967-103">AddressListId</span></span>

<span data-ttu-id="3d967-104">Das **AddressListId** -Element gibt den Bezeichner der einer Adressliste.</span><span class="sxs-lookup"><span data-stu-id="3d967-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="3d967-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="3d967-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d967-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3d967-106">Attributes and elements</span></span>

<span data-ttu-id="3d967-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3d967-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d967-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d967-108">Attributes</span></span>

|<span data-ttu-id="3d967-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3d967-109">**Attribute**</span></span>|<span data-ttu-id="3d967-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d967-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d967-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="3d967-111">**Id**</span></span> <br/> |<span data-ttu-id="3d967-112">Ein String-Adresse listenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3d967-112">A string address list identifier.</span></span> <span data-ttu-id="3d967-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3d967-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3d967-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d967-114">Child elements</span></span>

<span data-ttu-id="3d967-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d967-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d967-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d967-116">Parent elements</span></span>

|<span data-ttu-id="3d967-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3d967-117">**Element**</span></span>|<span data-ttu-id="3d967-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d967-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d967-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="3d967-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="3d967-120">Gibt den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d967-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="3d967-121">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen von Zustand "gelesen" für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3d967-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="3d967-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="3d967-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="3d967-123">Gibt den Bezeichner des Ordners, der e-Mail-Elemente kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d967-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="3d967-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="3d967-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="3d967-125">Gibt den Zielordner für die Kopie an, und verschieben Sie Aktionen.</span><span class="sxs-lookup"><span data-stu-id="3d967-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="3d967-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="3d967-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="3d967-127">Gibt den Bezeichner des Ordners in den e-Mail-Elemente verschoben werden</span><span class="sxs-lookup"><span data-stu-id="3d967-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d967-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d967-128">Remarks</span></span>

<span data-ttu-id="3d967-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3d967-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3d967-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3d967-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d967-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3d967-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d967-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d967-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3d967-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3d967-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3d967-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="3d967-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="3d967-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3d967-135">Validation File</span></span>  <br/> |<span data-ttu-id="3d967-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3d967-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3d967-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3d967-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3d967-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d967-138">See also</span></span>

- [<span data-ttu-id="3d967-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3d967-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

