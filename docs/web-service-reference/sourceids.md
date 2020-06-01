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
description: Das SourceIds-Element enthält die Quellbezeichner, die konvertiert werden sollen.
ms.openlocfilehash: 1c4990f2185788c5cfaab5483cb6a54a0d850596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466108"
---
# <a name="sourceids"></a><span data-ttu-id="bd97a-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="bd97a-103">SourceIds</span></span>

<span data-ttu-id="bd97a-104">Das **SourceIds** -Element enthält die Quellbezeichner, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd97a-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="bd97a-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="bd97a-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="bd97a-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="bd97a-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="bd97a-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="bd97a-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd97a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd97a-108">Attributes and elements</span></span>

<span data-ttu-id="bd97a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd97a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd97a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd97a-110">Attributes</span></span>

<span data-ttu-id="bd97a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd97a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd97a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd97a-112">Child elements</span></span>

|<span data-ttu-id="bd97a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd97a-113">**Element**</span></span>|<span data-ttu-id="bd97a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd97a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd97a-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="bd97a-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="bd97a-116">Beschreibt eine Element-oder Ordner-ID, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd97a-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="bd97a-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="bd97a-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="bd97a-118">Beschreibt einen Bezeichner für Öffentliche Ordner, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd97a-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="bd97a-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="bd97a-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="bd97a-120">Beschreibt einen Elementbezeichner für Öffentliche Ordner, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd97a-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd97a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd97a-121">Parent elements</span></span>

|<span data-ttu-id="bd97a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd97a-122">**Element**</span></span>|<span data-ttu-id="bd97a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd97a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd97a-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="bd97a-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="bd97a-125">Definiert eine Anforderung zum Konvertieren von Element-und Ordner Bezeichnern zwischen von Exchange unterstützten Formaten.</span><span class="sxs-lookup"><span data-stu-id="bd97a-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd97a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd97a-126">Remarks</span></span>

<span data-ttu-id="bd97a-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd97a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd97a-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bd97a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd97a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd97a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bd97a-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd97a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="bd97a-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bd97a-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bd97a-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bd97a-132">Validation File</span></span>  <br/> |<span data-ttu-id="bd97a-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bd97a-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bd97a-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bd97a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd97a-135">False</span><span class="sxs-lookup"><span data-stu-id="bd97a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd97a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd97a-136">See also</span></span>



[<span data-ttu-id="bd97a-137">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bd97a-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="bd97a-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bd97a-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="bd97a-139">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="bd97a-139">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

