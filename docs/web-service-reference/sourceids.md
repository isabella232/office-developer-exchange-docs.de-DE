---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: Das SourceIds-Element enthält die Source-Bezeichner konvertiert.
ms.openlocfilehash: c9ee9fd01367f714e1cb3770e2be5161cb45d98f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831522"
---
# <a name="sourceids"></a><span data-ttu-id="11008-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="11008-103">SourceIds</span></span>

<span data-ttu-id="11008-104">Das **SourceIds** -Element enthält die Source-Bezeichner konvertiert.</span><span class="sxs-lookup"><span data-stu-id="11008-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="11008-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="11008-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="11008-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="11008-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="11008-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="11008-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11008-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="11008-108">Attributes and elements</span></span>

<span data-ttu-id="11008-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="11008-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11008-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="11008-110">Attributes</span></span>

<span data-ttu-id="11008-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="11008-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11008-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11008-112">Child elements</span></span>

|<span data-ttu-id="11008-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="11008-113">**Element**</span></span>|<span data-ttu-id="11008-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11008-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11008-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="11008-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="11008-116">Beschreibt einen Bezeichner Elements oder Ordners zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11008-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="11008-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="11008-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="11008-118">Beschreibt einen Bezeichner für Öffentliche Ordner zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11008-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="11008-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="11008-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="11008-120">Beschreibt einen Bezeichner für Öffentliche Ordner zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11008-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11008-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11008-121">Parent elements</span></span>

|<span data-ttu-id="11008-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="11008-122">**Element**</span></span>|<span data-ttu-id="11008-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11008-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11008-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="11008-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="11008-125">Definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange unterstützt Formate konvertieren.</span><span class="sxs-lookup"><span data-stu-id="11008-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11008-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11008-126">Remarks</span></span>

<span data-ttu-id="11008-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="11008-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11008-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="11008-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11008-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="11008-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="11008-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="11008-130">Schema Name</span></span>  <br/> |<span data-ttu-id="11008-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="11008-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="11008-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="11008-132">Validation File</span></span>  <br/> |<span data-ttu-id="11008-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="11008-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="11008-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="11008-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="11008-135">False</span><span class="sxs-lookup"><span data-stu-id="11008-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11008-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11008-136">See also</span></span>



[<span data-ttu-id="11008-137">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="11008-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="11008-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="11008-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="11008-139">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="11008-139">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

