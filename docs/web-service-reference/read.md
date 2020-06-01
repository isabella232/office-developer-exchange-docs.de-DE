---
title: Read
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
description: Das Read-Element gibt an, ob ein Client einen Ordner oder ein Element lesen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: d75285e0ab14c4f53d73cb7f4349196e07c3c521
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468313"
---
# <a name="read"></a><span data-ttu-id="b7fa3-104">Read</span><span class="sxs-lookup"><span data-stu-id="b7fa3-104">Read</span></span>

<span data-ttu-id="b7fa3-105">Das **Read** -Element gibt an, ob ein Client einen Ordner oder ein Element lesen kann.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="b7fa3-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="b7fa3-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="b7fa3-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7fa3-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b7fa3-108">Attributes and elements</span></span>

<span data-ttu-id="b7fa3-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7fa3-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b7fa3-110">Attributes</span></span>

<span data-ttu-id="b7fa3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7fa3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7fa3-112">Child elements</span></span>

<span data-ttu-id="b7fa3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7fa3-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7fa3-114">Parent elements</span></span>

|<span data-ttu-id="b7fa3-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7fa3-115">**Element**</span></span>|<span data-ttu-id="b7fa3-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7fa3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7fa3-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b7fa3-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b7fa3-118">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="b7fa3-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7fa3-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="b7fa3-120">Text value</span></span>

<span data-ttu-id="b7fa3-121">Der Textwert **true** gibt an, dass ein Client ein Element des Ordners lesen kann.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7fa3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7fa3-122">Remarks</span></span>

<span data-ttu-id="b7fa3-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b7fa3-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7fa3-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b7fa3-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7fa3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7fa3-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7fa3-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b7fa3-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b7fa3-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b7fa3-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b7fa3-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b7fa3-128">Validation File</span></span>  <br/> |<span data-ttu-id="b7fa3-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b7fa3-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7fa3-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b7fa3-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7fa3-131">False</span><span class="sxs-lookup"><span data-stu-id="b7fa3-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7fa3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7fa3-132">See also</span></span>



- [<span data-ttu-id="b7fa3-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b7fa3-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b7fa3-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="b7fa3-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

