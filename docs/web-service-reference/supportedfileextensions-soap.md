---
title: SupportedFileExtensions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53
description: Das SupportedFileExtensions-Element enthält die Dateierweiterungen, die in einem Dokument sharing-Location gespeichert werden können.
ms.openlocfilehash: 0f1dbbce2b836fe05e4bc612c607302783d5e05d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839141"
---
# <a name="supportedfileextensions-soap"></a><span data-ttu-id="36000-103">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36000-103">SupportedFileExtensions (SOAP)</span></span>

<span data-ttu-id="36000-104">Das **SupportedFileExtensions** -Element enthält die Dateierweiterungen, die in einem Dokument sharing-Location gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="36000-104">The **SupportedFileExtensions** element lists the file extensions that can be stored in a document sharing location.</span></span> 
  
```XML
<SupportedFileExtensions /> 
```

 <span data-ttu-id="36000-105">**ArrayOfFileExtension**</span><span class="sxs-lookup"><span data-stu-id="36000-105">**ArrayOfFileExtension**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36000-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="36000-106">Attributes and elements</span></span>

<span data-ttu-id="36000-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="36000-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36000-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="36000-108">Attributes</span></span>

<span data-ttu-id="36000-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="36000-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36000-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36000-110">Child elements</span></span>

|<span data-ttu-id="36000-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="36000-111">**Element**</span></span>|<span data-ttu-id="36000-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36000-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36000-113">FileExtension (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36000-113">FileExtension (SOAP)</span></span>](fileextension-soap.md) <br/> |<span data-ttu-id="36000-114">Stellt eine Erweiterung dar.</span><span class="sxs-lookup"><span data-stu-id="36000-114">Represents a file extension.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36000-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36000-115">Parent elements</span></span>

|<span data-ttu-id="36000-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="36000-116">**Element**</span></span>|<span data-ttu-id="36000-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36000-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36000-118">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36000-118">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="36000-119">Stellt Informationen zum Standort und Metadaten für ein Dokument sharing-Location.</span><span class="sxs-lookup"><span data-stu-id="36000-119">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="36000-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="36000-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36000-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="36000-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="36000-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="36000-122">Schema Name</span></span>  <br/> |<span data-ttu-id="36000-123">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="36000-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="36000-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="36000-124">Validation File</span></span>  <br/> |<span data-ttu-id="36000-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36000-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36000-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="36000-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="36000-127">True</span><span class="sxs-lookup"><span data-stu-id="36000-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36000-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36000-128">See also</span></span>



[<span data-ttu-id="36000-129">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36000-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="36000-130">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="36000-130">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="36000-131">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="36000-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

