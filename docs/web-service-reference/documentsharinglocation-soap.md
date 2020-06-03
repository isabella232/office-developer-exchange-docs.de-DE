---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: Das DocumentSharingLocation-Element enthält Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort.
ms.openlocfilehash: 6fed933da979ab3e3fca51ba606127b7f0a4e3f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457060"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="d34c7-103">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="d34c7-104">Das **DocumentSharingLocation** -Element enthält Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d34c7-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
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

 <span data-ttu-id="d34c7-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="d34c7-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d34c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d34c7-106">Attributes and elements</span></span>

<span data-ttu-id="d34c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d34c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d34c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d34c7-108">Attributes</span></span>

<span data-ttu-id="d34c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d34c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d34c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d34c7-110">Child elements</span></span>

|<span data-ttu-id="d34c7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d34c7-111">**Element**</span></span>|<span data-ttu-id="d34c7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d34c7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d34c7-113">ServiceUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="d34c7-114">Stellt die URL des Dokumentfreigabe-Webdiensts dar.</span><span class="sxs-lookup"><span data-stu-id="d34c7-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-115">LocationUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="d34c7-116">Stellt die URL des Speicherorts für die Dokumentfreigabe dar.</span><span class="sxs-lookup"><span data-stu-id="d34c7-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-117">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="d34c7-118">Stellt den Namen des Dokumentfreigabe Speicherorts dar, der in der Benutzeroberfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d34c7-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-119">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="d34c7-120">Stellt die Dateierweiterungen dar, die am Dokumentfreigabe Speicherort gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="d34c7-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-121">ExternalAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="d34c7-122">Gibt an, ob der Speicherort der Dokumentfreigabe für externe Verbindungen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d34c7-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-123">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="d34c7-124">Gibt an, ob für den Zugriff auf den Freigabespeicherort ein authentifizierter Benutzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d34c7-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-125">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="d34c7-126">Gibt an, ob der Benutzerzugriffsberechtigungen für den Speicherort der Dokumentfreigabe ändern kann.</span><span class="sxs-lookup"><span data-stu-id="d34c7-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="d34c7-127">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="d34c7-128">Gibt an, ob der Speicherort für die Dokumentfreigabe der Standardfreigabe Speicherort des Benutzers ist.</span><span class="sxs-lookup"><span data-stu-id="d34c7-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d34c7-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d34c7-129">Parent elements</span></span>

|<span data-ttu-id="d34c7-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="d34c7-130">**Element**</span></span>|<span data-ttu-id="d34c7-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d34c7-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d34c7-132">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="d34c7-133">Enthält eine Liste der Speicherorte und Metadaten für die Freigabe von Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="d34c7-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d34c7-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="d34c7-134">Text value</span></span>

<span data-ttu-id="d34c7-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="d34c7-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d34c7-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d34c7-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d34c7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d34c7-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d34c7-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d34c7-138">Schema Name</span></span>  <br/> |<span data-ttu-id="d34c7-139">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="d34c7-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d34c7-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d34c7-140">Validation File</span></span>  <br/> |<span data-ttu-id="d34c7-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d34c7-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d34c7-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d34c7-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="d34c7-143">True</span><span class="sxs-lookup"><span data-stu-id="d34c7-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d34c7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d34c7-144">See also</span></span>

- [<span data-ttu-id="d34c7-145">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d34c7-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="d34c7-146">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="d34c7-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="d34c7-147">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d34c7-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

