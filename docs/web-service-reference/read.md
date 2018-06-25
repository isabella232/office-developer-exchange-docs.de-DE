---
title: Lesen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Read
api_type:
- schema
ms.assetid: b14637e9-1695-4b7e-b078-ae527c2e4303
description: Das Lesen-Element gibt an, ob ein Client eines Ordners oder Element lesen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: cd9c2c9802c78b202418e3947f5b5718b0f676cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830948"
---
# <a name="read"></a><span data-ttu-id="35372-104">Lesen</span><span class="sxs-lookup"><span data-stu-id="35372-104">Read</span></span>

<span data-ttu-id="35372-105">Das **Lesen** -Element gibt an, ob ein Client eines Ordners oder Element lesen kann.</span><span class="sxs-lookup"><span data-stu-id="35372-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="35372-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="35372-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="35372-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="35372-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35372-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35372-108">Attributes and elements</span></span>

<span data-ttu-id="35372-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="35372-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35372-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="35372-110">Attributes</span></span>

<span data-ttu-id="35372-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="35372-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35372-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35372-112">Child elements</span></span>

<span data-ttu-id="35372-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="35372-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35372-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35372-114">Parent elements</span></span>

|<span data-ttu-id="35372-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="35372-115">**Element**</span></span>|<span data-ttu-id="35372-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35372-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35372-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="35372-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="35372-118">Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="35372-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="35372-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="35372-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35372-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="35372-120">Text value</span></span>

<span data-ttu-id="35372-121">Der Textwert **true** gibt an, dass ein Client ein Element des Ordners lesen kann.</span><span class="sxs-lookup"><span data-stu-id="35372-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35372-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35372-122">Remarks</span></span>

<span data-ttu-id="35372-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="35372-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35372-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="35372-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35372-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="35372-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35372-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="35372-126">Schema Name</span></span>  <br/> |<span data-ttu-id="35372-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="35372-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="35372-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="35372-128">Validation File</span></span>  <br/> |<span data-ttu-id="35372-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35372-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35372-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="35372-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="35372-131">False</span><span class="sxs-lookup"><span data-stu-id="35372-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35372-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35372-132">See also</span></span>



- [<span data-ttu-id="35372-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="35372-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="35372-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="35372-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

