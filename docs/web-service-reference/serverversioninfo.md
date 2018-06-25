---
title: ServerVersionInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: Das Element ServerVersionInfo stellt die Versionsnummer von Microsoft Exchange Server.
ms.openlocfilehash: aff8a6542e2ae6fb1148dd29051b7b33ad90eeff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831389"
---
# <a name="serverversioninfo"></a><span data-ttu-id="c5f2a-103">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c5f2a-103">ServerVersionInfo</span></span>

<span data-ttu-id="c5f2a-104">Das Element **ServerVersionInfo** stellt die Versionsnummer von Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-104">The **ServerVersionInfo** element represents the Microsoft Exchange Server version number.</span></span> 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c5f2a-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f2a-105">Attributes and elements</span></span>

<span data-ttu-id="c5f2a-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5f2a-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5f2a-107">Attributes</span></span>

|<span data-ttu-id="c5f2a-108">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c5f2a-108">**Attribute**</span></span>|<span data-ttu-id="c5f2a-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5f2a-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5f2a-110">Hauptversion</span><span class="sxs-lookup"><span data-stu-id="c5f2a-110">MajorVersion</span></span>  <br/> |<span data-ttu-id="c5f2a-111">Beschreibt die Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-111">Describes the major version number.</span></span>  <br/> |
|<span data-ttu-id="c5f2a-112">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="c5f2a-112">MinorVersion</span></span>  <br/> |<span data-ttu-id="c5f2a-113">Beschreibt die Nummer der Nebenversion.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-113">Describes the minor version number.</span></span>  <br/> |
|<span data-ttu-id="c5f2a-114">MajorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="c5f2a-114">MajorBuildNumber</span></span>  <br/> |<span data-ttu-id="c5f2a-115">Beschreibt die wichtigsten Buildnummer an.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-115">Describes the major build number.</span></span>  <br/> |
|<span data-ttu-id="c5f2a-116">MinorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="c5f2a-116">MinorBuildNumber</span></span>  <br/> |<span data-ttu-id="c5f2a-117">Beschreibt die Nebenversion Buildnummer an.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-117">Describes the minor build number.</span></span>  <br/> |
|<span data-ttu-id="c5f2a-118">Version</span><span class="sxs-lookup"><span data-stu-id="c5f2a-118">Version</span></span>  <br/> |<span data-ttu-id="c5f2a-119">Beschreibt die Schemaversion von Exchange-Webdienste (EWS).</span><span class="sxs-lookup"><span data-stu-id="c5f2a-119">Describes the Exchange Web Services (EWS) schema version.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5f2a-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f2a-120">Child elements</span></span>

<span data-ttu-id="c5f2a-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5f2a-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f2a-122">Parent elements</span></span>

<span data-ttu-id="c5f2a-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5f2a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5f2a-124">Remarks</span></span>

<span data-ttu-id="c5f2a-125">Dieses Element wird in den SOAP-Header einer Exchange-Webdienste-Response-Nachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-125">This element is returned in the SOAP header of an Exchange Web Services response message.</span></span>
  
<span data-ttu-id="c5f2a-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5f2a-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c5f2a-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c5f2a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5f2a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5f2a-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5f2a-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5f2a-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c5f2a-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c5f2a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5f2a-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5f2a-131">Validation File</span></span>  <br/> |<span data-ttu-id="c5f2a-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5f2a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5f2a-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c5f2a-133">Can Be Empty</span></span>  <br/> |<span data-ttu-id="c5f2a-134">False</span><span class="sxs-lookup"><span data-stu-id="c5f2a-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5f2a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5f2a-135">See also</span></span>



- [<span data-ttu-id="c5f2a-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c5f2a-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

