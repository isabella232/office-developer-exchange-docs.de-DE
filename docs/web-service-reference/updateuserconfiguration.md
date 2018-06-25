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
description: Das Element UpdateUserConfiguration stellt eine Anforderung zum Aktualisieren einer Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: 54415677786d8d5b6579f42e6d384c087099ce03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839400"
---
# <a name="updateuserconfiguration"></a><span data-ttu-id="70d13-103">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="70d13-103">UpdateUserConfiguration</span></span>

<span data-ttu-id="70d13-104">Das Element **UpdateUserConfiguration** stellt eine Anforderung zum Aktualisieren einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="70d13-104">The **UpdateUserConfiguration** element represents a request to update a user configuration object.</span></span> 
  
```XML
<UpdateUserConfiguration>
   <UserConfiguration/>
</UpdateUserConfiguration>
```

 <span data-ttu-id="70d13-105">**UpdateUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="70d13-105">**UpdateUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70d13-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70d13-106">Attributes and elements</span></span>

<span data-ttu-id="70d13-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70d13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70d13-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="70d13-108">Attributes</span></span>

<span data-ttu-id="70d13-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="70d13-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70d13-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70d13-110">Child elements</span></span>

|<span data-ttu-id="70d13-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="70d13-111">**Element**</span></span>|<span data-ttu-id="70d13-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70d13-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70d13-113">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="70d13-113">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="70d13-114">Definiert einen einzelnen Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="70d13-114">Defines a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70d13-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70d13-115">Parent elements</span></span>

<span data-ttu-id="70d13-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="70d13-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="70d13-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="70d13-117">Text value</span></span>

<span data-ttu-id="70d13-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="70d13-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70d13-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70d13-119">Remarks</span></span>

<span data-ttu-id="70d13-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="70d13-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70d13-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70d13-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70d13-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="70d13-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="70d13-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70d13-123">Schema Name</span></span>  <br/> |<span data-ttu-id="70d13-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="70d13-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="70d13-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70d13-125">Validation File</span></span>  <br/> |<span data-ttu-id="70d13-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="70d13-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="70d13-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="70d13-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="70d13-128">False</span><span class="sxs-lookup"><span data-stu-id="70d13-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70d13-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70d13-129">See also</span></span>



- [<span data-ttu-id="70d13-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="70d13-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

