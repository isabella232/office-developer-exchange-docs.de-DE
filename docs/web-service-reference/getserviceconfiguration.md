---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: Das GetServiceConfiguration-Element definiert eine GetServiceConfiguration-Anforderung.
ms.openlocfilehash: e9357a9e3be22e129c4910c01231f9dbd22a2dbe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457872"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="7f4dd-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f4dd-103">GetServiceConfiguration</span></span>

<span data-ttu-id="7f4dd-104">Das **GetServiceConfiguration** -Element definiert eine GetServiceConfiguration-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="7f4dd-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f4dd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7f4dd-106">Attributes and elements</span></span>

<span data-ttu-id="7f4dd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f4dd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f4dd-108">Attributes</span></span>

<span data-ttu-id="7f4dd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7f4dd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f4dd-110">Child elements</span></span>

|<span data-ttu-id="7f4dd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-111">**Element**</span></span>|<span data-ttu-id="7f4dd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f4dd-113">Actingies</span><span class="sxs-lookup"><span data-stu-id="7f4dd-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="7f4dd-114">Gibt an, wen der Anrufer sendet.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="7f4dd-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-115">This element is optional.</span></span> <span data-ttu-id="7f4dd-116">Wenn dieses Element nicht vorhanden ist, wird der authentifizierte Benutzer als Absender angenommen.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="7f4dd-117">Das **actings** -Element muss enthalten sein, um Absender Hinweise anzufordern.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="7f4dd-118">Ein ErrorInvalidArgument-Fehler kann in einer Antwort zurückgegeben werden, wenn das **actings** -Element fehlt, keinen Routingtyp enthält, keine e-Mail-Adresse enthält, eine ungültige e-Mail-Adresse auflöst, für einen Benutzer in Active Directory-Domänendienste (AD DS) nicht aufgelöst wird oder in AD DS in mehrere Benutzer aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="7f4dd-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f4dd-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="7f4dd-120">Enthält die angeforderten Dienstkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-120">Contains the requested service configurations.</span></span> <span data-ttu-id="7f4dd-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7f4dd-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f4dd-122">Parent elements</span></span>

<span data-ttu-id="7f4dd-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7f4dd-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="7f4dd-124">Text value</span></span>

<span data-ttu-id="7f4dd-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f4dd-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f4dd-126">Remarks</span></span>

<span data-ttu-id="7f4dd-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7f4dd-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f4dd-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7f4dd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f4dd-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f4dd-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7f4dd-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7f4dd-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7f4dd-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7f4dd-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7f4dd-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7f4dd-132">Validation File</span></span>  <br/> |<span data-ttu-id="7f4dd-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7f4dd-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7f4dd-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7f4dd-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7f4dd-135">False</span><span class="sxs-lookup"><span data-stu-id="7f4dd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f4dd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f4dd-136">See also</span></span>



- [<span data-ttu-id="7f4dd-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7f4dd-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

