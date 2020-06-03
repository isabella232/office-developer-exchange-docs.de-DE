---
title: SupportedFileExtensions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53
description: Das SupportedFileExtensions-Element listet die Dateierweiterungen auf, die in einem Dokumentfreigabe Speicherort gespeichert werden können.
ms.openlocfilehash: d783b147a25ebbe3bff59c2142012b50bd80004e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44433987"
---
# <a name="supportedfileextensions-soap"></a><span data-ttu-id="3b04a-103">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b04a-103">SupportedFileExtensions (SOAP)</span></span>

<span data-ttu-id="3b04a-104">Das **SupportedFileExtensions** -Element listet die Dateierweiterungen auf, die in einem Dokumentfreigabe Speicherort gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="3b04a-104">The **SupportedFileExtensions** element lists the file extensions that can be stored in a document sharing location.</span></span> 
  
```XML
<SupportedFileExtensions /> 
```

 <span data-ttu-id="3b04a-105">**ArrayOfFileExtension**</span><span class="sxs-lookup"><span data-stu-id="3b04a-105">**ArrayOfFileExtension**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b04a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04a-106">Attributes and elements</span></span>

<span data-ttu-id="3b04a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b04a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b04a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b04a-108">Attributes</span></span>

<span data-ttu-id="3b04a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b04a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b04a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04a-110">Child elements</span></span>

|<span data-ttu-id="3b04a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b04a-111">**Element**</span></span>|<span data-ttu-id="3b04a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b04a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b04a-113">Dateierweiterung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b04a-113">FileExtension (SOAP)</span></span>](fileextension-soap.md) <br/> |<span data-ttu-id="3b04a-114">Stellt eine Dateierweiterung dar.</span><span class="sxs-lookup"><span data-stu-id="3b04a-114">Represents a file extension.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b04a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04a-115">Parent elements</span></span>

|<span data-ttu-id="3b04a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b04a-116">**Element**</span></span>|<span data-ttu-id="3b04a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b04a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b04a-118">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b04a-118">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="3b04a-119">Stellt Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort dar.</span><span class="sxs-lookup"><span data-stu-id="3b04a-119">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="3b04a-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b04a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b04a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b04a-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3b04a-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b04a-122">Schema Name</span></span>  <br/> |<span data-ttu-id="3b04a-123">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="3b04a-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3b04a-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b04a-124">Validation File</span></span>  <br/> |<span data-ttu-id="3b04a-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3b04a-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b04a-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b04a-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b04a-127">True</span><span class="sxs-lookup"><span data-stu-id="3b04a-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b04a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b04a-128">See also</span></span>



[<span data-ttu-id="3b04a-129">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b04a-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="3b04a-130">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="3b04a-130">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="3b04a-131">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3b04a-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

