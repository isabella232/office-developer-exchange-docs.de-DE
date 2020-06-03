---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: Das ExchangeStoreId-Element gibt den Chatgruppen Bezeichner (Instant Messaging) an.
ms.openlocfilehash: c1b1e1830987449eeb7ea186d00743ea9cc75a77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456990"
---
# <a name="exchangestoreid"></a><span data-ttu-id="a6838-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="a6838-103">ExchangeStoreId</span></span>

<span data-ttu-id="a6838-104">Das **ExchangeStoreId** -Element gibt den Chatgruppen Bezeichner (Instant Messaging) an.</span><span class="sxs-lookup"><span data-stu-id="a6838-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="a6838-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="a6838-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6838-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6838-106">Attributes and elements</span></span>

<span data-ttu-id="a6838-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6838-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6838-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6838-108">Attributes</span></span>

|<span data-ttu-id="a6838-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a6838-109">**Attribute**</span></span>|<span data-ttu-id="a6838-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6838-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6838-111">Id</span><span class="sxs-lookup"><span data-stu-id="a6838-111">Id</span></span>  <br/> |<span data-ttu-id="a6838-112">Der Textwert des **ID-** Attributs ist der Bezeichner der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a6838-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="a6838-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="a6838-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="a6838-114">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a6838-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a6838-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6838-115">Child elements</span></span>

<span data-ttu-id="a6838-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6838-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6838-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6838-117">Parent elements</span></span>

|<span data-ttu-id="a6838-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6838-118">**Element**</span></span>|<span data-ttu-id="a6838-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6838-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6838-120">Imgroup</span><span class="sxs-lookup"><span data-stu-id="a6838-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="a6838-121">Stellt eine Sofortnachrichten Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="a6838-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6838-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6838-122">Remarks</span></span>

<span data-ttu-id="a6838-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a6838-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a6838-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a6838-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6838-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a6838-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6838-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6838-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6838-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6838-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a6838-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="a6838-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="a6838-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6838-129">Validation File</span></span>  <br/> |<span data-ttu-id="a6838-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a6838-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6838-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a6838-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a6838-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6838-132">See also</span></span>



- [<span data-ttu-id="a6838-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a6838-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

