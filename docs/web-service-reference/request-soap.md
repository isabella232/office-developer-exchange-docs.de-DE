---
title: Anforderung (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: Das angeforderte Element enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.
ms.openlocfilehash: dfea33786066dd7803d0fd061cbb87bb06d11531
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831125"
---
# <a name="request-soap"></a><span data-ttu-id="496da-103">Anforderung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-103">Request (SOAP)</span></span>

<span data-ttu-id="496da-104">Das Element **Anforderung** enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="496da-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="496da-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="496da-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="496da-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="496da-106">Attributes and elements</span></span>

<span data-ttu-id="496da-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="496da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="496da-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="496da-108">Attributes</span></span>

<span data-ttu-id="496da-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="496da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="496da-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="496da-110">Child elements</span></span>

|<span data-ttu-id="496da-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="496da-111">**Element**</span></span>|<span data-ttu-id="496da-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="496da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="496da-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="496da-114">Stellt eine Auflistung von E-mail-Adressen der Benutzer für die Einstellungen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="496da-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="496da-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="496da-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="496da-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="496da-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="496da-118">Gibt die bestimmten Server-Version, die der Anbieter verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="496da-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="496da-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="496da-119">Parent elements</span></span>

|<span data-ttu-id="496da-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="496da-120">**Element**</span></span>|<span data-ttu-id="496da-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="496da-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="496da-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="496da-123">Stellt eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="496da-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="496da-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="496da-124">Text value</span></span>

<span data-ttu-id="496da-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="496da-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="496da-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="496da-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="496da-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="496da-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="496da-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="496da-128">Schema Name</span></span>  <br/> |<span data-ttu-id="496da-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="496da-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="496da-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="496da-130">Validation File</span></span>  <br/> |<span data-ttu-id="496da-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="496da-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="496da-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="496da-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="496da-133">True</span><span class="sxs-lookup"><span data-stu-id="496da-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="496da-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="496da-134">See also</span></span>



[<span data-ttu-id="496da-135">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="496da-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

