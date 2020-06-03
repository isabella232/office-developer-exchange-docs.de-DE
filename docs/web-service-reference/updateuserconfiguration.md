---
title: UpdateUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateUserConfiguration
api_type:
- schema
ms.assetid: ccf7c577-f882-477e-9f6f-2f56729f7d77
description: Das UpdateUserConfiguration-Element stellt eine Anforderung zum Aktualisieren eines Benutzer Konfigurationsobjekts dar.
ms.openlocfilehash: b46552dc93523340b04f4abfb07dc4fca7dd7898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468831"
---
# <a name="updateuserconfiguration"></a><span data-ttu-id="18b0c-103">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="18b0c-103">UpdateUserConfiguration</span></span>

<span data-ttu-id="18b0c-104">Das **UpdateUserConfiguration** -Element stellt eine Anforderung zum Aktualisieren eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="18b0c-104">The **UpdateUserConfiguration** element represents a request to update a user configuration object.</span></span> 
  
```XML
<UpdateUserConfiguration>
   <UserConfiguration/>
</UpdateUserConfiguration>
```

 <span data-ttu-id="18b0c-105">**UpdateUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="18b0c-105">**UpdateUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18b0c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18b0c-106">Attributes and elements</span></span>

<span data-ttu-id="18b0c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18b0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18b0c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="18b0c-108">Attributes</span></span>

<span data-ttu-id="18b0c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="18b0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18b0c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18b0c-110">Child elements</span></span>

|<span data-ttu-id="18b0c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="18b0c-111">**Element**</span></span>|<span data-ttu-id="18b0c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18b0c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18b0c-113">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="18b0c-113">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="18b0c-114">Definiert ein einzelnes Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="18b0c-114">Defines a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18b0c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18b0c-115">Parent elements</span></span>

<span data-ttu-id="18b0c-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="18b0c-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="18b0c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="18b0c-117">Text value</span></span>

<span data-ttu-id="18b0c-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="18b0c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18b0c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18b0c-119">Remarks</span></span>

<span data-ttu-id="18b0c-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="18b0c-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18b0c-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18b0c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18b0c-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="18b0c-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18b0c-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18b0c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="18b0c-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="18b0c-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18b0c-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18b0c-125">Validation File</span></span>  <br/> |<span data-ttu-id="18b0c-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18b0c-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18b0c-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="18b0c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="18b0c-128">False</span><span class="sxs-lookup"><span data-stu-id="18b0c-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18b0c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b0c-129">See also</span></span>



- [<span data-ttu-id="18b0c-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18b0c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

