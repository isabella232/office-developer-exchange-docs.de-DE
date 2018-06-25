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
description: Das UserConfigurationProperties-Element gibt die Eigenschaftentypen in einem Vorgang GetUserConfiguration abgerufen.
ms.openlocfilehash: 4f993765bb7c36f28a41a3f2fa7e28698a3f709e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839440"
---
# <a name="userconfigurationproperties"></a><span data-ttu-id="fffa7-103">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="fffa7-103">UserConfigurationProperties</span></span>

<span data-ttu-id="fffa7-104">Das **UserConfigurationProperties** -Element gibt die Eigenschaftentypen in einem Vorgang GetUserConfiguration abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fffa7-104">The **UserConfigurationProperties** element specifies the property types to get in a GetUserConfiguration operation.</span></span> 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 <span data-ttu-id="fffa7-105">**UserConfigurationPropertyType**</span><span class="sxs-lookup"><span data-stu-id="fffa7-105">**UserConfigurationPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fffa7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fffa7-106">Attributes and elements</span></span>

<span data-ttu-id="fffa7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fffa7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fffa7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fffa7-108">Attributes</span></span>

<span data-ttu-id="fffa7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fffa7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fffa7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fffa7-110">Child elements</span></span>

<span data-ttu-id="fffa7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fffa7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fffa7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fffa7-112">Parent elements</span></span>

|<span data-ttu-id="fffa7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fffa7-113">**Element**</span></span>|<span data-ttu-id="fffa7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fffa7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fffa7-115">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="fffa7-115">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="fffa7-116">Gibt eine Anforderung zum Abrufen einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="fffa7-116">Specifies a request to get a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fffa7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="fffa7-117">Text value</span></span>

<span data-ttu-id="fffa7-118">Die folgende Tabelle enthält die möglichen Werte für das **UserConfigurationProperties** -Element.</span><span class="sxs-lookup"><span data-stu-id="fffa7-118">The following table lists the possible values for the **UserConfigurationProperties** element.</span></span> 
  
|<span data-ttu-id="fffa7-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fffa7-119">**Value**</span></span>|<span data-ttu-id="fffa7-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fffa7-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fffa7-121">Id</span><span class="sxs-lookup"><span data-stu-id="fffa7-121">Id</span></span>  <br/> |<span data-ttu-id="fffa7-122">Gibt die ID-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="fffa7-122">Specifies the identifier property.</span></span>  <br/> |
|<span data-ttu-id="fffa7-123">Dictionary</span><span class="sxs-lookup"><span data-stu-id="fffa7-123">Dictionary</span></span>  <br/> |<span data-ttu-id="fffa7-124">Gibt die Eigenschaftentypen Wörterbuch an.</span><span class="sxs-lookup"><span data-stu-id="fffa7-124">Specifies dictionary property types.</span></span>  <br/> |
|<span data-ttu-id="fffa7-125">XmlData</span><span class="sxs-lookup"><span data-stu-id="fffa7-125">XmlData</span></span>  <br/> |<span data-ttu-id="fffa7-126">Gibt die Typen von XML-Daten an.</span><span class="sxs-lookup"><span data-stu-id="fffa7-126">Specifies XML data property types.</span></span>  <br/> |
|<span data-ttu-id="fffa7-127">BinaryData</span><span class="sxs-lookup"><span data-stu-id="fffa7-127">BinaryData</span></span>  <br/> |<span data-ttu-id="fffa7-128">Gibt Binärdaten Eigenschaftentypen.</span><span class="sxs-lookup"><span data-stu-id="fffa7-128">Specifies binary data property types.</span></span>  <br/> |
|<span data-ttu-id="fffa7-129">Alle</span><span class="sxs-lookup"><span data-stu-id="fffa7-129">All</span></span>  <br/> |<span data-ttu-id="fffa7-130">Gibt den Bezeichner, Wörterbuch, XML-Daten und Eigenschaftentypen Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="fffa7-130">Specifies the identifier, dictionary, XML data, and binary data property types.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fffa7-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fffa7-131">Remarks</span></span>

<span data-ttu-id="fffa7-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fffa7-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fffa7-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fffa7-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fffa7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="fffa7-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fffa7-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fffa7-135">Schema Name</span></span>  <br/> |<span data-ttu-id="fffa7-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fffa7-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fffa7-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fffa7-137">Validation File</span></span>  <br/> |<span data-ttu-id="fffa7-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fffa7-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fffa7-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fffa7-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="fffa7-140">False</span><span class="sxs-lookup"><span data-stu-id="fffa7-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fffa7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fffa7-141">See also</span></span>



- [<span data-ttu-id="fffa7-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fffa7-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

