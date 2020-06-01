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
description: Das ServerVersionInfo-Element stellt die Versionsnummer Exchange Server dar.
ms.openlocfilehash: 5bd1fbd8fdee584a9d272fa8ab82f2a31c1357fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466829"
---
# <a name="serverversioninfo"></a><span data-ttu-id="d6ee3-103">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d6ee3-103">ServerVersionInfo</span></span>

<span data-ttu-id="d6ee3-104">Das **ServerVersionInfo** -Element stellt die Versionsnummer Exchange Server dar.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-104">The **ServerVersionInfo** element represents the Microsoft Exchange Server version number.</span></span> 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d6ee3-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6ee3-105">Attributes and elements</span></span>

<span data-ttu-id="d6ee3-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6ee3-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6ee3-107">Attributes</span></span>

|<span data-ttu-id="d6ee3-108">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d6ee3-108">**Attribute**</span></span>|<span data-ttu-id="d6ee3-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6ee3-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6ee3-110">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="d6ee3-110">MajorVersion</span></span>  <br/> |<span data-ttu-id="d6ee3-111">Beschreibt die Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-111">Describes the major version number.</span></span>  <br/> |
|<span data-ttu-id="d6ee3-112">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="d6ee3-112">MinorVersion</span></span>  <br/> |<span data-ttu-id="d6ee3-113">Beschreibt die Nummer der Nebenversion.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-113">Describes the minor version number.</span></span>  <br/> |
|<span data-ttu-id="d6ee3-114">MajorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="d6ee3-114">MajorBuildNumber</span></span>  <br/> |<span data-ttu-id="d6ee3-115">Beschreibt die Hauptnummer des Builds.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-115">Describes the major build number.</span></span>  <br/> |
|<span data-ttu-id="d6ee3-116">MinorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="d6ee3-116">MinorBuildNumber</span></span>  <br/> |<span data-ttu-id="d6ee3-117">Beschreibt die Nebenversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-117">Describes the minor build number.</span></span>  <br/> |
|<span data-ttu-id="d6ee3-118">Version</span><span class="sxs-lookup"><span data-stu-id="d6ee3-118">Version</span></span>  <br/> |<span data-ttu-id="d6ee3-119">Beschreibt die Exchange-Webdienste Schemaversion.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-119">Describes the Exchange Web Services (EWS) schema version.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6ee3-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6ee3-120">Child elements</span></span>

<span data-ttu-id="d6ee3-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6ee3-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6ee3-122">Parent elements</span></span>

<span data-ttu-id="d6ee3-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6ee3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6ee3-124">Remarks</span></span>

<span data-ttu-id="d6ee3-125">Dieses Element wird im SOAP-Header einer Exchange Webdienste-Antwortnachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-125">This element is returned in the SOAP header of an Exchange Web Services response message.</span></span>
  
<span data-ttu-id="d6ee3-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d6ee3-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d6ee3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6ee3-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6ee3-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6ee3-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6ee3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="d6ee3-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d6ee3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6ee3-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6ee3-131">Validation File</span></span>  <br/> |<span data-ttu-id="d6ee3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6ee3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6ee3-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d6ee3-133">Can Be Empty</span></span>  <br/> |<span data-ttu-id="d6ee3-134">False</span><span class="sxs-lookup"><span data-stu-id="d6ee3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6ee3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6ee3-135">See also</span></span>



- [<span data-ttu-id="d6ee3-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6ee3-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

