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
description: Das GetUserSettingsRequest-Element stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.
ms.openlocfilehash: 353facb5d0bbf922a23b33cbaf6f9d2e7d82bd6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530162"
---
# <a name="getusersettingsrequest-soap"></a><span data-ttu-id="52ba5-103">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-103">GetUserSettingsRequest (SOAP)</span></span>

<span data-ttu-id="52ba5-104">Das **GetUserSettingsRequest** -Element stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="52ba5-104">The **GetUserSettingsRequest** element represents a request to retrieve specified settings for one or more users.</span></span> 
  
```XML
<GetUserSettingsRequest>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetUserSettingsRequest>
```

 <span data-ttu-id="52ba5-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="52ba5-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52ba5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52ba5-106">Attributes and elements</span></span>

<span data-ttu-id="52ba5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52ba5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52ba5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="52ba5-108">Attributes</span></span>

<span data-ttu-id="52ba5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="52ba5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52ba5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52ba5-110">Child elements</span></span>

|<span data-ttu-id="52ba5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="52ba5-111">**Element**</span></span>|<span data-ttu-id="52ba5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52ba5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52ba5-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="52ba5-114">Stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52ba5-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="52ba5-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="52ba5-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="52ba5-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="52ba5-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="52ba5-118">Gibt die spezifische Server Version an, die der Anbieter verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="52ba5-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52ba5-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52ba5-119">Parent elements</span></span>

<span data-ttu-id="52ba5-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="52ba5-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="52ba5-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="52ba5-121">Text value</span></span>

<span data-ttu-id="52ba5-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="52ba5-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52ba5-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="52ba5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52ba5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="52ba5-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="52ba5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52ba5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="52ba5-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="52ba5-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="52ba5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52ba5-127">Validation File</span></span>  <br/> |<span data-ttu-id="52ba5-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="52ba5-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52ba5-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="52ba5-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="52ba5-130">True</span><span class="sxs-lookup"><span data-stu-id="52ba5-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52ba5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52ba5-131">See also</span></span>



[<span data-ttu-id="52ba5-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="52ba5-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

