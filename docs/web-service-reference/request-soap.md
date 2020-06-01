---
title: Request (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: Das Request-Element enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.
ms.openlocfilehash: 4358713d19e763b75d2a43f147385026f43b1255
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448989"
---
# <a name="request-soap"></a><span data-ttu-id="6bf30-103">Request (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-103">Request (SOAP)</span></span>

<span data-ttu-id="6bf30-104">Das **Request** -Element enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="6bf30-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="6bf30-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="6bf30-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6bf30-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf30-106">Attributes and elements</span></span>

<span data-ttu-id="6bf30-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6bf30-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6bf30-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6bf30-108">Attributes</span></span>

<span data-ttu-id="6bf30-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6bf30-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6bf30-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf30-110">Child elements</span></span>

|<span data-ttu-id="6bf30-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bf30-111">**Element**</span></span>|<span data-ttu-id="6bf30-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf30-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bf30-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="6bf30-114">Stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bf30-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="6bf30-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="6bf30-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="6bf30-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="6bf30-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="6bf30-118">Gibt die spezifische Server Version an, die der Anbieter verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="6bf30-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6bf30-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf30-119">Parent elements</span></span>

|<span data-ttu-id="6bf30-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bf30-120">**Element**</span></span>|<span data-ttu-id="6bf30-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf30-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bf30-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="6bf30-123">Stellt eine [SOAP-Anforderung (GetUserSettings Operation)](getusersettings-operation-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="6bf30-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6bf30-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="6bf30-124">Text value</span></span>

<span data-ttu-id="6bf30-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="6bf30-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6bf30-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6bf30-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bf30-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bf30-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6bf30-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6bf30-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6bf30-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="6bf30-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6bf30-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6bf30-130">Validation File</span></span>  <br/> |<span data-ttu-id="6bf30-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6bf30-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6bf30-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6bf30-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6bf30-133">True</span><span class="sxs-lookup"><span data-stu-id="6bf30-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bf30-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bf30-134">See also</span></span>



[<span data-ttu-id="6bf30-135">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6bf30-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

