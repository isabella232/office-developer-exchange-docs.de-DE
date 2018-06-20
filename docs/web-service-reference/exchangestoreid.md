---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: Das ExchangeStoreId-Element gibt die Instant messaging (IM)-Gruppen-ID an.
ms.openlocfilehash: 815e9c2f368558ea38efce3671dbdc33d4d97168
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758303"
---
# <a name="exchangestoreid"></a><span data-ttu-id="28425-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="28425-103">ExchangeStoreId</span></span>

<span data-ttu-id="28425-104">Das **ExchangeStoreId** -Element gibt die Instant messaging (IM)-Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="28425-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="28425-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="28425-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28425-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28425-106">Attributes and elements</span></span>

<span data-ttu-id="28425-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28425-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28425-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28425-108">Attributes</span></span>

|<span data-ttu-id="28425-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="28425-109">**Attribute**</span></span>|<span data-ttu-id="28425-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28425-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28425-111">Id</span><span class="sxs-lookup"><span data-stu-id="28425-111">Id</span></span>  <br/> |<span data-ttu-id="28425-112">Der Textwert des **Id** -Attributs ist der Bezeichner der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="28425-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="28425-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="28425-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="28425-114">Der Textwert des **ChangeKey** -Attributs ist der Key Ändern der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="28425-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28425-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28425-115">Child elements</span></span>

<span data-ttu-id="28425-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="28425-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28425-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28425-117">Parent elements</span></span>

|<span data-ttu-id="28425-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="28425-118">**Element**</span></span>|<span data-ttu-id="28425-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28425-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28425-120">ImGroup</span><span class="sxs-lookup"><span data-stu-id="28425-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="28425-121">Stellt eine instant messaging-Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="28425-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28425-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28425-122">Remarks</span></span>

<span data-ttu-id="28425-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28425-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="28425-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="28425-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28425-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28425-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28425-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="28425-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28425-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28425-127">Schema Name</span></span>  <br/> |<span data-ttu-id="28425-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="28425-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="28425-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28425-129">Validation File</span></span>  <br/> |<span data-ttu-id="28425-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28425-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="28425-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="28425-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="28425-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28425-132">See also</span></span>



- [<span data-ttu-id="28425-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28425-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

