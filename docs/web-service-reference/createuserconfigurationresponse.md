---
title: CreateUserConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfigurationResponse
api_type:
- schema
ms.assetid: 115d4a5d-0c90-45d5-a3a3-4e61d80df78a
description: Das CreateUserConfigurationResponse-Element definiert eine Antwort auf eine einzelne CreateUserConfiguration-Anforderung.
ms.openlocfilehash: d1b3e2a0ab156c5175f9c1e676866690c33ace9f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463769"
---
# <a name="createuserconfigurationresponse"></a><span data-ttu-id="4fb45-103">CreateUserConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="4fb45-103">CreateUserConfigurationResponse</span></span>

<span data-ttu-id="4fb45-104">Das **CreateUserConfigurationResponse** -Element definiert eine Antwort auf eine einzelne **CreateUserConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4fb45-104">The **CreateUserConfigurationResponse** element defines a response to a single **CreateUserConfiguration** request.</span></span> 
  
```xml
<CreateUserConfigurationResponse>
   <ResponseMessages/>
</CreateUserConfigurationResponse>
```

 <span data-ttu-id="4fb45-105">**CreateUserConfigurationResponseType**</span><span class="sxs-lookup"><span data-stu-id="4fb45-105">**CreateUserConfigurationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fb45-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4fb45-106">Attributes and elements</span></span>

<span data-ttu-id="4fb45-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4fb45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fb45-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fb45-108">Attributes</span></span>

<span data-ttu-id="4fb45-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fb45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fb45-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fb45-110">Child elements</span></span>

|<span data-ttu-id="4fb45-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fb45-111">**Element**</span></span>|<span data-ttu-id="4fb45-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fb45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fb45-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4fb45-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4fb45-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4fb45-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4fb45-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fb45-115">Parent elements</span></span>

<span data-ttu-id="4fb45-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fb45-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4fb45-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="4fb45-117">Text value</span></span>

<span data-ttu-id="4fb45-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fb45-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fb45-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fb45-119">Remarks</span></span>

<span data-ttu-id="4fb45-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4fb45-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fb45-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4fb45-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fb45-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fb45-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4fb45-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4fb45-123">Schema Name</span></span>  <br/> |<span data-ttu-id="4fb45-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4fb45-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4fb45-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4fb45-125">Validation File</span></span>  <br/> |<span data-ttu-id="4fb45-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4fb45-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4fb45-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4fb45-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="4fb45-128">False</span><span class="sxs-lookup"><span data-stu-id="4fb45-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fb45-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb45-129">See also</span></span>



- [<span data-ttu-id="4fb45-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4fb45-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

