---
title: DeleteUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfiguration
api_type:
- schema
ms.assetid: 91b18b6a-d904-476c-996d-b041e859da1e
description: Das DeleteUserConfiguration-Element stellt eine Anforderung zum Löschen eines Benutzer Konfigurationsobjekts dar.
ms.openlocfilehash: 04668ead48e7c321ed7e91cbbeb67c6154c02283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460757"
---
# <a name="deleteuserconfiguration"></a><span data-ttu-id="4538f-103">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="4538f-103">DeleteUserConfiguration</span></span>

<span data-ttu-id="4538f-104">Das **DeleteUserConfiguration** -Element stellt eine Anforderung zum Löschen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="4538f-104">The **DeleteUserConfiguration** element represents a request to delete a user configuration object.</span></span> 
  
```xml
<DeleteUserConfiguration>
   <UserConfigurationName/>
</DeleteUserConfiguration>
```

 <span data-ttu-id="4538f-105">**DeleteUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="4538f-105">**DeleteUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4538f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4538f-106">Attributes and elements</span></span>

<span data-ttu-id="4538f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4538f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4538f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4538f-108">Attributes</span></span>

<span data-ttu-id="4538f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4538f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4538f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4538f-110">Child elements</span></span>

|<span data-ttu-id="4538f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4538f-111">**Element**</span></span>|<span data-ttu-id="4538f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4538f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4538f-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4538f-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="4538f-114">Stellt den Namen des zu löschenden Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="4538f-114">Represents the name of the user configuration object to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4538f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4538f-115">Parent elements</span></span>

<span data-ttu-id="4538f-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4538f-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4538f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="4538f-117">Text value</span></span>

<span data-ttu-id="4538f-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="4538f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4538f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4538f-119">Remarks</span></span>

<span data-ttu-id="4538f-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4538f-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4538f-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4538f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4538f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="4538f-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4538f-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4538f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="4538f-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4538f-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4538f-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4538f-125">Validation File</span></span>  <br/> |<span data-ttu-id="4538f-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4538f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4538f-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4538f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="4538f-128">False</span><span class="sxs-lookup"><span data-stu-id="4538f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4538f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4538f-129">See also</span></span>

- [<span data-ttu-id="4538f-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4538f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

