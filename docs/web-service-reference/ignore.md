---
title: Ignorieren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ignore
api_type:
- schema
ms.assetid: 7789eec5-ceec-43f2-84d5-d0d15b734076
description: Das Ignore-Element identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen.
ms.openlocfilehash: b65d11d8c7655279dac0e7d3cbd13f8a9317540c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458572"
---
# <a name="ignore"></a><span data-ttu-id="d0cdc-103">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d0cdc-103">Ignore</span></span>

<span data-ttu-id="d0cdc-104">Das **Ignore** -Element identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="d0cdc-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d0cdc-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="d0cdc-106">Ignore</span><span class="sxs-lookup"><span data-stu-id="d0cdc-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="d0cdc-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="d0cdc-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0cdc-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0cdc-108">Attributes and elements</span></span>

<span data-ttu-id="d0cdc-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0cdc-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0cdc-110">Attributes</span></span>

<span data-ttu-id="d0cdc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0cdc-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0cdc-112">Child elements</span></span>

|<span data-ttu-id="d0cdc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0cdc-113">**Element**</span></span>|<span data-ttu-id="d0cdc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0cdc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0cdc-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d0cdc-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d0cdc-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0cdc-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0cdc-117">Parent elements</span></span>

|<span data-ttu-id="d0cdc-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0cdc-118">**Element**</span></span>|<span data-ttu-id="d0cdc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0cdc-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0cdc-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d0cdc-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="d0cdc-121">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0cdc-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0cdc-122">Remarks</span></span>

<span data-ttu-id="d0cdc-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d0cdc-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0cdc-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0cdc-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0cdc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0cdc-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0cdc-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0cdc-126">Schema name</span></span>  <br/> |<span data-ttu-id="d0cdc-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d0cdc-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0cdc-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0cdc-128">Validation file</span></span>  <br/> |<span data-ttu-id="d0cdc-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d0cdc-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0cdc-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d0cdc-130">Can be empty</span></span>  <br/> |<span data-ttu-id="d0cdc-131">False</span><span class="sxs-lookup"><span data-stu-id="d0cdc-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0cdc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0cdc-132">See also</span></span>



[<span data-ttu-id="d0cdc-133">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0cdc-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d0cdc-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0cdc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

