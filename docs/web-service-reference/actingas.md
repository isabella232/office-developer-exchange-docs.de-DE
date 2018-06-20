---
title: ActingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: Das ActingAs-Element identifiziert, die der Anrufer als sendet.
ms.openlocfilehash: 9c007ed45f85dba265261dd79a6fd846dbd9d2f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758394"
---
# <a name="actingas"></a><span data-ttu-id="32085-103">ActingAs</span><span class="sxs-lookup"><span data-stu-id="32085-103">ActingAs</span></span>

<span data-ttu-id="32085-104">Das **ActingAs** -Element identifiziert, die der Anrufer als sendet.</span><span class="sxs-lookup"><span data-stu-id="32085-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="32085-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="32085-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32085-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32085-106">Attributes and elements</span></span>

<span data-ttu-id="32085-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32085-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32085-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32085-108">Attributes</span></span>

<span data-ttu-id="32085-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32085-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32085-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32085-110">Child elements</span></span>

|<span data-ttu-id="32085-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32085-111">**Element**</span></span>|<span data-ttu-id="32085-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32085-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32085-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="32085-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="32085-p101">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32085-p101">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="32085-116">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="32085-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="32085-p102">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32085-p102">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32085-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32085-120">Parent elements</span></span>

|<span data-ttu-id="32085-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="32085-121">**Element**</span></span>|<span data-ttu-id="32085-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32085-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32085-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="32085-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="32085-124">Definiert eine **GetServiceConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="32085-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32085-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32085-125">Remarks</span></span>

<span data-ttu-id="32085-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32085-126">This element is optional.</span></span> <span data-ttu-id="32085-127">Wenn dieses Element nicht vorhanden ist, wird davon ausgegangen, dass der authentifizierte Benutzer die Absender werden.</span><span class="sxs-lookup"><span data-stu-id="32085-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="32085-128">Das **ActingAs** -Element muss für die Anforderung des Absenders Hinweise eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="32085-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="32085-129">Fehler **ErrorInvalidArgument** kann in einer Antwort zurückgegeben werden soll, wenn das **ActingAs** -Element nicht vorhanden ist, enthält keine Routingtyp, eine e-Mail-Adresse nicht umfasst, eine ungültige e-Mail-Adresse enthält, nicht an einen Benutzer in Active Directory löst -Domänendienste (AD DS), oder löst auf mehrere Benutzer in AD DS.</span><span class="sxs-lookup"><span data-stu-id="32085-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="32085-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="32085-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32085-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="32085-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32085-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="32085-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="32085-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32085-133">Schema Name</span></span>  <br/> |<span data-ttu-id="32085-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="32085-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="32085-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32085-135">Validation File</span></span>  <br/> |<span data-ttu-id="32085-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="32085-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32085-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="32085-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="32085-138">False</span><span class="sxs-lookup"><span data-stu-id="32085-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32085-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32085-139">See also</span></span>

- [<span data-ttu-id="32085-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="32085-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

