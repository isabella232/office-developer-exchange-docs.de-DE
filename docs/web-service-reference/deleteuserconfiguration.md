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
description: Das Element DeleteUserConfiguration stellt eine Anforderung zum Löschen einer Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: e357c32f95cddc866b77b6f1172ab260837b061b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757931"
---
# <a name="deleteuserconfiguration"></a><span data-ttu-id="5abb4-103">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="5abb4-103">DeleteUserConfiguration</span></span>

<span data-ttu-id="5abb4-104">Das Element **DeleteUserConfiguration** stellt eine Anforderung zum Löschen einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5abb4-104">The **DeleteUserConfiguration** element represents a request to delete a user configuration object.</span></span> 
  
```xml
<DeleteUserConfiguration>
   <UserConfigurationName/>
</DeleteUserConfiguration>
```

 <span data-ttu-id="5abb4-105">**DeleteUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="5abb4-105">**DeleteUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5abb4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5abb4-106">Attributes and elements</span></span>

<span data-ttu-id="5abb4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5abb4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5abb4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5abb4-108">Attributes</span></span>

<span data-ttu-id="5abb4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5abb4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5abb4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5abb4-110">Child elements</span></span>

|<span data-ttu-id="5abb4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5abb4-111">**Element**</span></span>|<span data-ttu-id="5abb4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5abb4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5abb4-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5abb4-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="5abb4-114">Den Namen des zu löschenden Objekts Konfiguration Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5abb4-114">Represents the name of the user configuration object to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5abb4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5abb4-115">Parent elements</span></span>

<span data-ttu-id="5abb4-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="5abb4-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5abb4-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5abb4-117">Text value</span></span>

<span data-ttu-id="5abb4-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="5abb4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5abb4-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5abb4-119">Remarks</span></span>

<span data-ttu-id="5abb4-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5abb4-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5abb4-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5abb4-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5abb4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5abb4-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5abb4-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5abb4-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5abb4-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5abb4-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5abb4-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5abb4-125">Validation File</span></span>  <br/> |<span data-ttu-id="5abb4-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5abb4-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5abb4-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5abb4-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5abb4-128">False</span><span class="sxs-lookup"><span data-stu-id="5abb4-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5abb4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5abb4-129">See also</span></span>

- [<span data-ttu-id="5abb4-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5abb4-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

