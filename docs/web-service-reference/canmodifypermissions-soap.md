---
title: CanModifyPermissions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: Das CanModifyPermissions-Element gibt an, ob ein Benutzer zu einem Dokument sharing-Location Zugriffsberechtigungen ändern kann.
ms.openlocfilehash: 16526cb79eeca591af6e009e67959a1c3b58a5d7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757550"
---
# <a name="canmodifypermissions-soap"></a><span data-ttu-id="dc70b-103">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc70b-103">CanModifyPermissions (SOAP)</span></span>

<span data-ttu-id="dc70b-104">Das **CanModifyPermissions** -Element gibt an, ob ein Benutzer zu einem Dokument sharing-Location Zugriffsberechtigungen ändern kann.</span><span class="sxs-lookup"><span data-stu-id="dc70b-104">The **CanModifyPermissions** element indicates whether a user can modify access permissions to a document sharing location.</span></span> 
  
```XML
<CanModifyPermissions /> 
```

 <span data-ttu-id="dc70b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc70b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc70b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc70b-106">Attributes and elements</span></span>

<span data-ttu-id="dc70b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc70b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc70b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc70b-108">Attributes</span></span>

<span data-ttu-id="dc70b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc70b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc70b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc70b-110">Child elements</span></span>

<span data-ttu-id="dc70b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc70b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc70b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc70b-112">Parent elements</span></span>

|<span data-ttu-id="dc70b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc70b-113">**Element**</span></span>|<span data-ttu-id="dc70b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc70b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc70b-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc70b-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="dc70b-116">Stellt Informationen zum Standort und Metadaten für ein Dokument sharing-Location.</span><span class="sxs-lookup"><span data-stu-id="dc70b-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc70b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="dc70b-117">Text value</span></span>

<span data-ttu-id="dc70b-118">Der boolesche Wert des **CanModifyPermissions** -Elements gibt an, ob Benutzer Zugriffsberechtigungen für den freigegebenen Speicherort ändern können.</span><span class="sxs-lookup"><span data-stu-id="dc70b-118">The Boolean value of the **CanModifyPermissions** element indicates whether users can modify access permissions to the sharing location.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="dc70b-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc70b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc70b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc70b-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="dc70b-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc70b-121">Schema Name</span></span>  <br/> |<span data-ttu-id="dc70b-122">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="dc70b-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="dc70b-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc70b-123">Validation File</span></span>  <br/> |<span data-ttu-id="dc70b-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dc70b-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc70b-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dc70b-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc70b-126">True</span><span class="sxs-lookup"><span data-stu-id="dc70b-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc70b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc70b-127">See also</span></span>



[<span data-ttu-id="dc70b-128">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc70b-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="dc70b-129">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="dc70b-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="dc70b-130">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="dc70b-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

