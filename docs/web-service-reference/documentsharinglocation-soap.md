---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: Das DocumentSharingLocation-Element enthält, Speicherort und Metadateninformationen für ein Dokument sharing-Location.
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758082"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="cd8b9-103">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="cd8b9-104">Das **DocumentSharingLocation** -Element enthält, Speicherort und Metadateninformationen für ein Dokument sharing-Location.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 <span data-ttu-id="cd8b9-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="cd8b9-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd8b9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8b9-106">Attributes and elements</span></span>

<span data-ttu-id="cd8b9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd8b9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd8b9-108">Attributes</span></span>

<span data-ttu-id="cd8b9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd8b9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8b9-110">Child elements</span></span>

|<span data-ttu-id="cd8b9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd8b9-111">**Element**</span></span>|<span data-ttu-id="cd8b9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd8b9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd8b9-113">ServiceUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="cd8b9-114">Stellt die URL des Dokuments Freigabe-Webdienst.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-115">LocationUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="cd8b9-116">Stellt die URL des Dokuments sharing-Location.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-117">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="cd8b9-118">Stellt den Namen des Dokuments sharing-Location in der Benutzeroberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-119">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="cd8b9-120">Stellt die Dateierweiterungen, die im Dokument sharing-Location gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-121">ExternalAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="cd8b9-122">Gibt an, ob das Dokument sharing-Location außerhalb Verbindungen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-123">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="cd8b9-124">Gibt an, ob der Zugriff auf den freigegebenen Speicherort als authentifizierten Benutzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-125">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="cd8b9-126">Gibt an, ob der Benutzer die Zugriffsberechtigungen für das Dokument sharing-Location ändern kann.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="cd8b9-127">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="cd8b9-128">Gibt an, ob das Dokument sharing-Location des Benutzers Standard sharing-Location ist.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd8b9-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8b9-129">Parent elements</span></span>

|<span data-ttu-id="cd8b9-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd8b9-130">**Element**</span></span>|<span data-ttu-id="cd8b9-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd8b9-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd8b9-132">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="cd8b9-133">Enthält eine Liste der Dokumentfreigabe Speicherorte und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd8b9-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="cd8b9-134">Text value</span></span>

<span data-ttu-id="cd8b9-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd8b9-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd8b9-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cd8b9-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd8b9-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd8b9-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cd8b9-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd8b9-138">Schema Name</span></span>  <br/> |<span data-ttu-id="cd8b9-139">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="cd8b9-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cd8b9-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd8b9-140">Validation File</span></span>  <br/> |<span data-ttu-id="cd8b9-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd8b9-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd8b9-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cd8b9-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd8b9-143">True</span><span class="sxs-lookup"><span data-stu-id="cd8b9-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd8b9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd8b9-144">See also</span></span>

- [<span data-ttu-id="cd8b9-145">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cd8b9-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="cd8b9-146">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="cd8b9-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="cd8b9-147">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="cd8b9-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

