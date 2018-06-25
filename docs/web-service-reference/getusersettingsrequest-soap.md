---
title: GetUserSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 832a9211-d2d5-4a49-bcb3-1dc6dc3904ed
description: Das Element GetUserSettingsRequest stellt eine Anforderung an die angegebene Einstellungen für einen oder mehrere Benutzer abzurufen.
ms.openlocfilehash: dc22570144a6947dc6e7042326c7416422680cc1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829702"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="c0482-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0482-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="c0482-104">Das Element **GetUserSettingsRequest** stellt eine Anforderung an die angegebene Einstellungen für einen oder mehrere Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0482-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="c0482-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="c0482-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0482-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0482-106">Attributes and elements</span></span>

<span data-ttu-id="c0482-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0482-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0482-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0482-108">Attributes</span></span>

<span data-ttu-id="c0482-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0482-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0482-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0482-110">Child elements</span></span>

|<span data-ttu-id="c0482-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0482-111">**Element**</span></span>|<span data-ttu-id="c0482-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0482-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0482-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0482-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="c0482-114">Stellt eine Auflistung von E-mail-Adressen der Benutzer für die Einstellungen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0482-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="c0482-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0482-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="c0482-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c0482-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="c0482-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0482-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="c0482-118">Gibt die bestimmten Server-Version, die der Anbieter verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c0482-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0482-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0482-119">Parent elements</span></span>

<span data-ttu-id="c0482-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0482-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c0482-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="c0482-121">Text value</span></span>

<span data-ttu-id="c0482-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0482-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0482-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0482-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0482-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0482-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c0482-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0482-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c0482-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="c0482-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c0482-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0482-127">Validation File</span></span>  <br/> |<span data-ttu-id="c0482-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0482-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0482-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0482-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0482-130">True</span><span class="sxs-lookup"><span data-stu-id="c0482-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0482-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0482-131">See also</span></span>



[<span data-ttu-id="c0482-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0482-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

