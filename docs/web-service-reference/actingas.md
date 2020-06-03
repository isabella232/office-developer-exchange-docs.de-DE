---
title: Actingies
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
description: Das actings-Element identifiziert, wen der Anrufer sendet.
ms.openlocfilehash: 175a03018ee3529ec595dbe9afb7dc61ad6afc35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529700"
---
# <a name="actingas"></a><span data-ttu-id="b7a72-103">Actingies</span><span class="sxs-lookup"><span data-stu-id="b7a72-103">ActingAs</span></span>

<span data-ttu-id="b7a72-104">Das **actings** -Element identifiziert, wen der Anrufer sendet.</span><span class="sxs-lookup"><span data-stu-id="b7a72-104">The **ActingAs** element identifies who the caller is sending as.</span></span> 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 <span data-ttu-id="b7a72-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="b7a72-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7a72-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b7a72-106">Attributes and elements</span></span>

<span data-ttu-id="b7a72-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b7a72-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7a72-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b7a72-108">Attributes</span></span>

<span data-ttu-id="b7a72-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7a72-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7a72-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7a72-110">Child elements</span></span>

|<span data-ttu-id="b7a72-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7a72-111">**Element**</span></span>|<span data-ttu-id="b7a72-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7a72-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7a72-113">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b7a72-113">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="b7a72-p101">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7a72-p101">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="b7a72-116">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="b7a72-116">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="b7a72-p102">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7a72-p102">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7a72-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7a72-120">Parent elements</span></span>

|<span data-ttu-id="b7a72-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7a72-121">**Element**</span></span>|<span data-ttu-id="b7a72-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7a72-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7a72-123">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7a72-123">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="b7a72-124">Definiert eine **GetServiceConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b7a72-124">Defines a **GetServiceConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7a72-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7a72-125">Remarks</span></span>

<span data-ttu-id="b7a72-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7a72-126">This element is optional.</span></span> <span data-ttu-id="b7a72-127">Wenn dieses Element nicht vorhanden ist, wird der authentifizierte Benutzer als Absender angenommen.</span><span class="sxs-lookup"><span data-stu-id="b7a72-127">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="b7a72-128">Das **actings** -Element muss enthalten sein, um Absender Hinweise anzufordern.</span><span class="sxs-lookup"><span data-stu-id="b7a72-128">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="b7a72-129">Ein **ErrorInvalidArgument** -Fehler kann in einer Antwort zurückgegeben werden, wenn das **actings** -Element fehlt, keinen Routingtyp enthält, keine e-Mail-Adresse enthält, eine ungültige e-Mail-Adresse auflöst, für einen Benutzer in Active Directory-Domänendienste (AD DS) nicht aufgelöst wird oder in AD DS in mehrere Benutzer aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b7a72-129">An **ErrorInvalidArgument** error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span> 
  
<span data-ttu-id="b7a72-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b7a72-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7a72-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b7a72-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7a72-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7a72-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7a72-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b7a72-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b7a72-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b7a72-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7a72-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b7a72-135">Validation File</span></span>  <br/> |<span data-ttu-id="b7a72-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b7a72-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7a72-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b7a72-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7a72-138">False</span><span class="sxs-lookup"><span data-stu-id="b7a72-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7a72-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7a72-139">See also</span></span>

- [<span data-ttu-id="b7a72-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b7a72-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

