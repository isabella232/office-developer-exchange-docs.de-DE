---
title: CreateUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfiguration
api_type:
- schema
ms.assetid: 43e12e8b-5629-4f5f-9cbd-a99084d8460f
description: Das CreateUserConfiguration-Element stellt eine Anforderung zum Erstellen eines Benutzer Konfigurationsobjekts dar.
ms.openlocfilehash: 1d9194baf309936cb4be088a7ff56250dfa349cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463776"
---
# <a name="createuserconfiguration"></a><span data-ttu-id="23f7e-103">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="23f7e-103">CreateUserConfiguration</span></span>

<span data-ttu-id="23f7e-104">Das **CreateUserConfiguration** -Element stellt eine Anforderung zum Erstellen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="23f7e-104">The **CreateUserConfiguration** element represents a request to create a user configuration object.</span></span> 
  
```xml
<CreateUserConfiguration>
   <UserConfiguration/>
</CreateUserConfiguration>
```

 <span data-ttu-id="23f7e-105">**CreateUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="23f7e-105">**CreateUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23f7e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="23f7e-106">Attributes and elements</span></span>

<span data-ttu-id="23f7e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="23f7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23f7e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="23f7e-108">Attributes</span></span>

<span data-ttu-id="23f7e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="23f7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23f7e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23f7e-110">Child elements</span></span>

|<span data-ttu-id="23f7e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="23f7e-111">**Element**</span></span>|<span data-ttu-id="23f7e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23f7e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23f7e-113">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="23f7e-113">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="23f7e-114">Stellt ein einzelnes Benutzer Konfigurationsobjekt dar.</span><span class="sxs-lookup"><span data-stu-id="23f7e-114">Represents a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23f7e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23f7e-115">Parent elements</span></span>

<span data-ttu-id="23f7e-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="23f7e-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="23f7e-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="23f7e-117">Text value</span></span>

<span data-ttu-id="23f7e-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="23f7e-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23f7e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23f7e-119">Remarks</span></span>

<span data-ttu-id="23f7e-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="23f7e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23f7e-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="23f7e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23f7e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="23f7e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="23f7e-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="23f7e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="23f7e-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="23f7e-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="23f7e-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="23f7e-125">Validation File</span></span>  <br/> |<span data-ttu-id="23f7e-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="23f7e-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="23f7e-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="23f7e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="23f7e-128">False</span><span class="sxs-lookup"><span data-stu-id="23f7e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23f7e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23f7e-129">See also</span></span>



- [<span data-ttu-id="23f7e-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="23f7e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

