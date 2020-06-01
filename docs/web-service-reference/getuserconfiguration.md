---
title: GetUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 4044c0a1-cd88-41ae-9cc4-a7cf2b279094
description: Das GetUserConfiguration-Element stellt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts dar.
ms.openlocfilehash: 46a2a5ebbabfc038692a5de83e0a960e05295061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457711"
---
# <a name="getuserconfiguration"></a><span data-ttu-id="52878-103">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="52878-103">GetUserConfiguration</span></span>

<span data-ttu-id="52878-104">Das **GetUserConfiguration** -Element stellt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="52878-104">The **GetUserConfiguration** element represent a request to get a user configuration object.</span></span> 
  
```XML
<GetUserConfiguration>
   <UserConfigurationName/>
   <UserConfigurationProperties/>
</GetUserConfiguration>
```

 <span data-ttu-id="52878-105">**GetUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="52878-105">**GetUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52878-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52878-106">Attributes and elements</span></span>

<span data-ttu-id="52878-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52878-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52878-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="52878-108">Attributes</span></span>

<span data-ttu-id="52878-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="52878-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52878-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52878-110">Child elements</span></span>

|<span data-ttu-id="52878-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="52878-111">**Element**</span></span>|<span data-ttu-id="52878-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52878-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52878-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="52878-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="52878-114">Stellt den Namen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="52878-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="52878-115">Dieses Element muss in einer GetUserConfiguration-Anforderung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="52878-115">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
|[<span data-ttu-id="52878-116">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="52878-116">UserConfigurationProperties</span></span>](userconfigurationproperties.md) <br/> |<span data-ttu-id="52878-117">Gibt die zurückzugebenden Benutzer Konfigurationseigenschaften Typen an.</span><span class="sxs-lookup"><span data-stu-id="52878-117">Specifies the user configuration property types to return.</span></span> <span data-ttu-id="52878-118">Dieses Element muss in einer GetUserConfiguration-Anforderung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="52878-118">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52878-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52878-119">Parent elements</span></span>

<span data-ttu-id="52878-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="52878-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="52878-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="52878-121">Text value</span></span>

<span data-ttu-id="52878-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="52878-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52878-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52878-123">Remarks</span></span>

<span data-ttu-id="52878-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="52878-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52878-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="52878-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52878-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="52878-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52878-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52878-127">Schema Name</span></span>  <br/> |<span data-ttu-id="52878-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="52878-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52878-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52878-129">Validation File</span></span>  <br/> |<span data-ttu-id="52878-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="52878-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52878-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="52878-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="52878-132">False</span><span class="sxs-lookup"><span data-stu-id="52878-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52878-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52878-133">See also</span></span>



- [<span data-ttu-id="52878-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="52878-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

