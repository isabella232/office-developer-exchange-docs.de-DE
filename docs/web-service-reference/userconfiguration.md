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
description: Das UserConfiguration-Element definiert einen einzelnen Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839437"
---
# <a name="userconfiguration"></a><span data-ttu-id="90112-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="90112-103">UserConfiguration</span></span>

<span data-ttu-id="90112-104">Das **UserConfiguration** -Element definiert einen einzelnen Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="90112-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="90112-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="90112-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90112-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="90112-106">Attributes and elements</span></span>

<span data-ttu-id="90112-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="90112-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90112-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="90112-108">Attributes</span></span>

<span data-ttu-id="90112-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="90112-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90112-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90112-110">Child elements</span></span>

|<span data-ttu-id="90112-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="90112-111">**Element**</span></span>|<span data-ttu-id="90112-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90112-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90112-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="90112-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="90112-114">Der Name eines Benutzers Configuration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="90112-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="90112-115">Dieses Element muss verwendet werden, wenn Sie eine Benutzer-Konfigurationsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="90112-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="90112-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="90112-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="90112-117">Definiert die Benutzer Konfiguration Element-ID an.</span><span class="sxs-lookup"><span data-stu-id="90112-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|[<span data-ttu-id="90112-118">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="90112-118">Dictionary</span></span>](dictionary.md) <br/> |<span data-ttu-id="90112-119">Definiert eine Reihe von Einträgen in Wörterbuch-Eigenschaft für eine Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="90112-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="90112-120">XmlData</span><span class="sxs-lookup"><span data-stu-id="90112-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="90112-121">Enthält Inhalt für die XML-Eigenschaft für eine Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="90112-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="90112-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="90112-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="90112-123">Enthält Inhalt von Binärdaten-Eigenschaft für eine Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="90112-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90112-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90112-124">Parent elements</span></span>

|<span data-ttu-id="90112-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="90112-125">**Element**</span></span>|<span data-ttu-id="90112-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90112-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90112-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="90112-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="90112-128">Eine Anforderung zum Erstellen eines Benutzers Konfiguration-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="90112-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="90112-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="90112-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="90112-130">Stellt eine Antwort, die ein Benutzer Configuration-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="90112-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="90112-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="90112-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="90112-132">Stellt eine Anforderung zum Aktualisieren einer Benutzer-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="90112-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90112-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90112-133">Remarks</span></span>

<span data-ttu-id="90112-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="90112-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90112-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="90112-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90112-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="90112-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90112-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="90112-137">Schema Name</span></span>  <br/> |<span data-ttu-id="90112-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="90112-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="90112-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="90112-139">Validation File</span></span>  <br/> |<span data-ttu-id="90112-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="90112-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90112-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="90112-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="90112-142">False</span><span class="sxs-lookup"><span data-stu-id="90112-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90112-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90112-143">See also</span></span>



- [<span data-ttu-id="90112-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="90112-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

