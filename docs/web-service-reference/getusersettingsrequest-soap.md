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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829702"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="16bad-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="16bad-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="16bad-104">Das Element **GetUserSettingsRequest** stellt eine Anforderung an die angegebene Einstellungen für einen oder mehrere Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16bad-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="16bad-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="16bad-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16bad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="16bad-106">Attributes and elements</span></span>

<span data-ttu-id="16bad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="16bad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16bad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="16bad-108">Attributes</span></span>

<span data-ttu-id="16bad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="16bad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16bad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16bad-110">Child elements</span></span>

|<span data-ttu-id="16bad-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="16bad-111">**Element**</span></span>|<span data-ttu-id="16bad-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16bad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16bad-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="16bad-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="16bad-114">Stellt eine Auflistung von E-mail-Adressen der Benutzer für die Einstellungen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="16bad-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="16bad-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="16bad-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="16bad-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="16bad-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="16bad-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="16bad-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="16bad-118">Gibt die bestimmten Server-Version, die der Anbieter verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="16bad-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="16bad-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16bad-119">Parent elements</span></span>

<span data-ttu-id="16bad-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="16bad-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="16bad-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="16bad-121">Text value</span></span>

<span data-ttu-id="16bad-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="16bad-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16bad-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="16bad-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16bad-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="16bad-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="16bad-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="16bad-125">Schema Name</span></span>  <br/> |<span data-ttu-id="16bad-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="16bad-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="16bad-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="16bad-127">Validation File</span></span>  <br/> |<span data-ttu-id="16bad-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="16bad-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="16bad-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="16bad-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="16bad-130">True</span><span class="sxs-lookup"><span data-stu-id="16bad-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16bad-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16bad-131">See also</span></span>



[<span data-ttu-id="16bad-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="16bad-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

