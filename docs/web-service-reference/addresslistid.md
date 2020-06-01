---
title: AddressList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: Das AddressList-Element gibt den Bezeichner einer Adressliste an.
ms.openlocfilehash: c33944bf6e41903a5de596628e1ce7ba9f7421e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463608"
---
# <a name="addresslistid"></a><span data-ttu-id="7d99f-103">AddressList</span><span class="sxs-lookup"><span data-stu-id="7d99f-103">AddressListId</span></span>

<span data-ttu-id="7d99f-104">Das **AddressList** -Element gibt den Bezeichner einer Adressliste an.</span><span class="sxs-lookup"><span data-stu-id="7d99f-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="7d99f-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="7d99f-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d99f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7d99f-106">Attributes and elements</span></span>

<span data-ttu-id="7d99f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7d99f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d99f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d99f-108">Attributes</span></span>

|<span data-ttu-id="7d99f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7d99f-109">**Attribute**</span></span>|<span data-ttu-id="7d99f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d99f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d99f-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="7d99f-111">**Id**</span></span> <br/> |<span data-ttu-id="7d99f-112">Eine Zeichenfolgen-Adresslisten-ID.</span><span class="sxs-lookup"><span data-stu-id="7d99f-112">A string address list identifier.</span></span> <span data-ttu-id="7d99f-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d99f-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7d99f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d99f-114">Child elements</span></span>

<span data-ttu-id="7d99f-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d99f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d99f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d99f-116">Parent elements</span></span>

|<span data-ttu-id="7d99f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d99f-117">**Element**</span></span>|<span data-ttu-id="7d99f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d99f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d99f-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="7d99f-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="7d99f-120">Gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d99f-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="7d99f-121">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen des Lese Zustands für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7d99f-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="7d99f-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="7d99f-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="7d99f-123">Gibt den Bezeichner des Ordners an, in den e-Mail-Elemente kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d99f-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="7d99f-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="7d99f-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="7d99f-125">Gibt den Zielordner für die Aktionen kopieren und verlegen an.</span><span class="sxs-lookup"><span data-stu-id="7d99f-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="7d99f-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="7d99f-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="7d99f-127">Gibt den Bezeichner des Ordners an, in den e-Mail-Elemente verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7d99f-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d99f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d99f-128">Remarks</span></span>

<span data-ttu-id="7d99f-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7d99f-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7d99f-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7d99f-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d99f-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7d99f-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d99f-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d99f-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7d99f-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7d99f-133">Schema Name</span></span>  <br/> |<span data-ttu-id="7d99f-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="7d99f-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="7d99f-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7d99f-135">Validation File</span></span>  <br/> |<span data-ttu-id="7d99f-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7d99f-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7d99f-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7d99f-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7d99f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d99f-138">See also</span></span>

- [<span data-ttu-id="7d99f-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7d99f-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

