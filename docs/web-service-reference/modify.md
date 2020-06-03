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
description: Das Modify-Element gibt an, ob ein Client einen Ordner oder ein Element ändern kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e7712644ac9c32afab06be49b438ad83bbb31058
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530415"
---
# <a name="modify"></a><span data-ttu-id="0fa79-104">Ändern</span><span class="sxs-lookup"><span data-stu-id="0fa79-104">Modify</span></span>

<span data-ttu-id="0fa79-105">Das **Modify** -Element gibt an, ob ein Client einen Ordner oder ein Element ändern kann.</span><span class="sxs-lookup"><span data-stu-id="0fa79-105">The **Modify** element indicates whether a client can modify a folder or item.</span></span> <span data-ttu-id="0fa79-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0fa79-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Modify>true or false</Modify>
```

 <span data-ttu-id="0fa79-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="0fa79-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fa79-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0fa79-108">Attributes and elements</span></span>

<span data-ttu-id="0fa79-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0fa79-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fa79-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0fa79-110">Attributes</span></span>

<span data-ttu-id="0fa79-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fa79-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fa79-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fa79-112">Child elements</span></span>

<span data-ttu-id="0fa79-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fa79-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0fa79-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fa79-114">Parent elements</span></span>

|<span data-ttu-id="0fa79-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fa79-115">**Element**</span></span>|<span data-ttu-id="0fa79-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fa79-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fa79-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="0fa79-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="0fa79-118">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fa79-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="0fa79-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0fa79-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0fa79-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="0fa79-120">Text value</span></span>

<span data-ttu-id="0fa79-121">Der Textwert **true** gibt an, dass ein Client ein Element oder einen Ordner ändern kann.</span><span class="sxs-lookup"><span data-stu-id="0fa79-121">A text value of **true** indicates that a client can modify an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0fa79-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fa79-122">Remarks</span></span>

<span data-ttu-id="0fa79-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0fa79-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fa79-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0fa79-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fa79-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fa79-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0fa79-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0fa79-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0fa79-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0fa79-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0fa79-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0fa79-128">Validation File</span></span>  <br/> |<span data-ttu-id="0fa79-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0fa79-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0fa79-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0fa79-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fa79-131">False</span><span class="sxs-lookup"><span data-stu-id="0fa79-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fa79-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fa79-132">See also</span></span>



- [<span data-ttu-id="0fa79-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0fa79-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0fa79-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0fa79-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

