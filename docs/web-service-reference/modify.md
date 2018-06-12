---
title: Ändern
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Modify
api_type:
- schema
ms.assetid: 7a51e9e1-addb-4343-8a22-78f23763c0a8
description: Das Ändern-Element gibt an, ob ein Client eines Ordners oder Elements ändern kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 29fd2184e83f66a9b7e7db4173a765cee2922be8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830514"
---
# <a name="modify"></a><span data-ttu-id="ef05b-104">Ändern</span><span class="sxs-lookup"><span data-stu-id="ef05b-104">Modify</span></span>

<span data-ttu-id="ef05b-105">Das **Ändern** -Element gibt an, ob ein Client eines Ordners oder Elements ändern kann.</span><span class="sxs-lookup"><span data-stu-id="ef05b-105">The **Modify** element indicates whether a client can modify a folder or item.</span></span> <span data-ttu-id="ef05b-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef05b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Modify>true or false</Modify>
```

 <span data-ttu-id="ef05b-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="ef05b-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef05b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef05b-108">Attributes and elements</span></span>

<span data-ttu-id="ef05b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef05b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef05b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef05b-110">Attributes</span></span>

<span data-ttu-id="ef05b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef05b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef05b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef05b-112">Child elements</span></span>

<span data-ttu-id="ef05b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef05b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef05b-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef05b-114">Parent elements</span></span>

|<span data-ttu-id="ef05b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef05b-115">**Element**</span></span>|<span data-ttu-id="ef05b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef05b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef05b-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="ef05b-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="ef05b-118">Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="ef05b-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="ef05b-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef05b-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef05b-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="ef05b-120">Text value</span></span>

<span data-ttu-id="ef05b-121">Der Textwert **true** gibt an, dass ein Client eines Elements oder Ordners ändern kann.</span><span class="sxs-lookup"><span data-stu-id="ef05b-121">A text value of **true** indicates that a client can modify an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ef05b-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef05b-122">Remarks</span></span>

<span data-ttu-id="ef05b-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ef05b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef05b-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ef05b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef05b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef05b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef05b-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef05b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ef05b-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef05b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef05b-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef05b-128">Validation File</span></span>  <br/> |<span data-ttu-id="ef05b-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef05b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef05b-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef05b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef05b-131">False</span><span class="sxs-lookup"><span data-stu-id="ef05b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef05b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef05b-132">See also</span></span>



- [<span data-ttu-id="ef05b-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef05b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ef05b-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ef05b-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

