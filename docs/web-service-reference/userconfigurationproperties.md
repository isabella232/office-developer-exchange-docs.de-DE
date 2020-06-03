---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: Das UserConfigurationProperties-Element gibt die Eigenschaftentypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen.
ms.openlocfilehash: af6bee64516a7410d96ecc7581e8e819f550ddc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466493"
---
# <a name="userconfigurationproperties"></a><span data-ttu-id="d98ea-103">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="d98ea-103">UserConfigurationProperties</span></span>

<span data-ttu-id="d98ea-104">Das **UserConfigurationProperties** -Element gibt die Eigenschaftentypen an, die in einem GetUserConfiguration-Vorgang abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d98ea-104">The **UserConfigurationProperties** element specifies the property types to get in a GetUserConfiguration operation.</span></span> 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 <span data-ttu-id="d98ea-105">**UserConfigurationPropertyType**</span><span class="sxs-lookup"><span data-stu-id="d98ea-105">**UserConfigurationPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d98ea-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d98ea-106">Attributes and elements</span></span>

<span data-ttu-id="d98ea-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d98ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d98ea-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d98ea-108">Attributes</span></span>

<span data-ttu-id="d98ea-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d98ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d98ea-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d98ea-110">Child elements</span></span>

<span data-ttu-id="d98ea-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d98ea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d98ea-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d98ea-112">Parent elements</span></span>

|<span data-ttu-id="d98ea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d98ea-113">**Element**</span></span>|<span data-ttu-id="d98ea-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d98ea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d98ea-115">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="d98ea-115">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="d98ea-116">Gibt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-116">Specifies a request to get a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d98ea-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d98ea-117">Text value</span></span>

<span data-ttu-id="d98ea-118">In der folgenden Tabelle sind die möglichen Werte für das **UserConfigurationProperties** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d98ea-118">The following table lists the possible values for the **UserConfigurationProperties** element.</span></span> 
  
|<span data-ttu-id="d98ea-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d98ea-119">**Value**</span></span>|<span data-ttu-id="d98ea-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d98ea-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d98ea-121">Id</span><span class="sxs-lookup"><span data-stu-id="d98ea-121">Id</span></span>  <br/> |<span data-ttu-id="d98ea-122">Gibt die Identifier-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-122">Specifies the identifier property.</span></span>  <br/> |
|<span data-ttu-id="d98ea-123">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="d98ea-123">Dictionary</span></span>  <br/> |<span data-ttu-id="d98ea-124">Gibt Wörterbucheigenschaften Typen an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-124">Specifies dictionary property types.</span></span>  <br/> |
|<span data-ttu-id="d98ea-125">XMLDATA</span><span class="sxs-lookup"><span data-stu-id="d98ea-125">XmlData</span></span>  <br/> |<span data-ttu-id="d98ea-126">Gibt XML-Dateneigenschaften Typen an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-126">Specifies XML data property types.</span></span>  <br/> |
|<span data-ttu-id="d98ea-127">BinaryData</span><span class="sxs-lookup"><span data-stu-id="d98ea-127">BinaryData</span></span>  <br/> |<span data-ttu-id="d98ea-128">Gibt binäre Dateneigenschaften Typen an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-128">Specifies binary data property types.</span></span>  <br/> |
|<span data-ttu-id="d98ea-129">Alle</span><span class="sxs-lookup"><span data-stu-id="d98ea-129">All</span></span>  <br/> |<span data-ttu-id="d98ea-130">Gibt die Typenbezeichner, Wörterbuch, XML-Daten und Binärdaten an.</span><span class="sxs-lookup"><span data-stu-id="d98ea-130">Specifies the identifier, dictionary, XML data, and binary data property types.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d98ea-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d98ea-131">Remarks</span></span>

<span data-ttu-id="d98ea-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d98ea-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d98ea-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d98ea-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d98ea-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d98ea-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d98ea-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d98ea-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d98ea-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d98ea-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d98ea-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d98ea-137">Validation File</span></span>  <br/> |<span data-ttu-id="d98ea-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d98ea-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d98ea-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d98ea-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="d98ea-140">False</span><span class="sxs-lookup"><span data-stu-id="d98ea-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d98ea-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d98ea-141">See also</span></span>



- [<span data-ttu-id="d98ea-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d98ea-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

