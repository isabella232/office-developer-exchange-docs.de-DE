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
description: Das ignorieren-Element identifiziert Elemente, während der Synchronisierung zu überspringen.
ms.openlocfilehash: 0ecff9bfeb1257552b7e52c0115e9e814edecd4b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829858"
---
# <a name="ignore"></a><span data-ttu-id="f2d38-103">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f2d38-103">Ignore</span></span>

<span data-ttu-id="f2d38-104">Das **ignorieren** -Element identifiziert Elemente, während der Synchronisierung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="f2d38-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="f2d38-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="f2d38-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="f2d38-106">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f2d38-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="f2d38-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="f2d38-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2d38-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2d38-108">Attributes and elements</span></span>

<span data-ttu-id="f2d38-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2d38-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2d38-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2d38-110">Attributes</span></span>

<span data-ttu-id="f2d38-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2d38-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2d38-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2d38-112">Child elements</span></span>

|<span data-ttu-id="f2d38-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2d38-113">**Element**</span></span>|<span data-ttu-id="f2d38-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2d38-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d38-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f2d38-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f2d38-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f2d38-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2d38-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2d38-117">Parent elements</span></span>

|<span data-ttu-id="f2d38-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2d38-118">**Element**</span></span>|<span data-ttu-id="f2d38-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2d38-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d38-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="f2d38-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="f2d38-121">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f2d38-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2d38-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2d38-122">Remarks</span></span>

<span data-ttu-id="f2d38-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f2d38-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2d38-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f2d38-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2d38-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2d38-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2d38-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2d38-126">Schema name</span></span>  <br/> |<span data-ttu-id="f2d38-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f2d38-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2d38-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2d38-128">Validation file</span></span>  <br/> |<span data-ttu-id="f2d38-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2d38-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2d38-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f2d38-130">Can be empty</span></span>  <br/> |<span data-ttu-id="f2d38-131">False</span><span class="sxs-lookup"><span data-stu-id="f2d38-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2d38-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2d38-132">See also</span></span>



[<span data-ttu-id="f2d38-133">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f2d38-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="f2d38-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2d38-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

