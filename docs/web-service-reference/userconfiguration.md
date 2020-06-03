---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: Das UserConfiguration-Element definiert ein einzelnes Benutzer Konfigurationsobjekt.
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468908"
---
# <a name="userconfiguration"></a><span data-ttu-id="01bc6-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="01bc6-103">UserConfiguration</span></span>

<span data-ttu-id="01bc6-104">Das **UserConfiguration** -Element definiert ein einzelnes Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="01bc6-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="01bc6-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="01bc6-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01bc6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01bc6-106">Attributes and elements</span></span>

<span data-ttu-id="01bc6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01bc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01bc6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="01bc6-108">Attributes</span></span>

<span data-ttu-id="01bc6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="01bc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01bc6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01bc6-110">Child elements</span></span>

|<span data-ttu-id="01bc6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="01bc6-111">**Element**</span></span>|<span data-ttu-id="01bc6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01bc6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01bc6-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="01bc6-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="01bc6-114">Stellt den Namen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="01bc6-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="01bc6-115">Dieses Element muss verwendet werden, wenn Sie ein Benutzer Konfigurationsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="01bc6-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="01bc6-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="01bc6-117">Definiert die Element-ID des Benutzer Konfigurationsobjekts.</span><span class="sxs-lookup"><span data-stu-id="01bc6-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-118">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="01bc6-118">Dictionary</span></span>](dictionary.md) <br/> |<span data-ttu-id="01bc6-119">Definiert eine Gruppe von Wörterbuch-Eigenschafts Einträgen für ein Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="01bc6-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-120">XMLDATA</span><span class="sxs-lookup"><span data-stu-id="01bc6-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="01bc6-121">Enthält XML-Daten Eigenschafts Inhalt für ein Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="01bc6-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="01bc6-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="01bc6-123">Enthält binäre Daten Eigenschafts Inhalte für ein Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="01bc6-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01bc6-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01bc6-124">Parent elements</span></span>

|<span data-ttu-id="01bc6-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="01bc6-125">**Element**</span></span>|<span data-ttu-id="01bc6-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01bc6-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01bc6-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="01bc6-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="01bc6-128">Stellt eine Anforderung zum Erstellen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="01bc6-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="01bc6-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="01bc6-130">Stellt eine Antwort dar, die ein Benutzer Konfigurationsobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="01bc6-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="01bc6-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="01bc6-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="01bc6-132">Stellt eine Anforderung zum Aktualisieren eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="01bc6-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01bc6-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01bc6-133">Remarks</span></span>

<span data-ttu-id="01bc6-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="01bc6-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01bc6-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="01bc6-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01bc6-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="01bc6-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="01bc6-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01bc6-137">Schema Name</span></span>  <br/> |<span data-ttu-id="01bc6-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="01bc6-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="01bc6-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01bc6-139">Validation File</span></span>  <br/> |<span data-ttu-id="01bc6-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="01bc6-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="01bc6-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="01bc6-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="01bc6-142">False</span><span class="sxs-lookup"><span data-stu-id="01bc6-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01bc6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01bc6-143">See also</span></span>



- [<span data-ttu-id="01bc6-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="01bc6-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

