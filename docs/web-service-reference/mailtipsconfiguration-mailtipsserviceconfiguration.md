---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: Das MailTipsConfiguration-Element enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.
ms.openlocfilehash: ea92af3ebb2d2f720e5823c5317d09d5bcdb3978
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830321"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="119cd-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="119cd-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="119cd-104">Das **MailTipsConfiguration** -Element enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="119cd-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 <span data-ttu-id="119cd-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="119cd-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="119cd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="119cd-106">Attributes and elements</span></span>

<span data-ttu-id="119cd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="119cd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="119cd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="119cd-108">Attributes</span></span>

<span data-ttu-id="119cd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="119cd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="119cd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="119cd-110">Child elements</span></span>

|<span data-ttu-id="119cd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="119cd-111">**Element**</span></span>|<span data-ttu-id="119cd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="119cd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="119cd-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="119cd-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="119cd-114">Gibt an, ob der Mail-Tipps Dienst verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="119cd-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="119cd-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="119cd-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="119cd-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="119cd-117">Gibt die maximale Anzahl von Empfängern, die an den [GetMailTips Vorgang](getmailtips-operation.md)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="119cd-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="119cd-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="119cd-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="119cd-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="119cd-120">Stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="119cd-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="119cd-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="119cd-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="119cd-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="119cd-123">Stellt den Schwellenwert für die große Benutzergruppe für einen Client an.</span><span class="sxs-lookup"><span data-stu-id="119cd-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="119cd-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="119cd-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="119cd-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="119cd-126">Gibt an, ob Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="119cd-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="119cd-127">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="119cd-128">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="119cd-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="119cd-129">Gibt die Liste der internen SMTP-Domänen der Organisation.</span><span class="sxs-lookup"><span data-stu-id="119cd-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="119cd-130">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="119cd-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="119cd-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="119cd-131">Parent elements</span></span>

|<span data-ttu-id="119cd-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="119cd-132">**Element**</span></span>|<span data-ttu-id="119cd-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="119cd-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="119cd-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="119cd-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="119cd-135">Konfigurationseinstellungen für enthält.</span><span class="sxs-lookup"><span data-stu-id="119cd-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="119cd-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="119cd-136">Text value</span></span>

<span data-ttu-id="119cd-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="119cd-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="119cd-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="119cd-138">Remarks</span></span>

<span data-ttu-id="119cd-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="119cd-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="119cd-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="119cd-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="119cd-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="119cd-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="119cd-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="119cd-142">Schema Name</span></span>  <br/> |<span data-ttu-id="119cd-143">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="119cd-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="119cd-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="119cd-144">Validation File</span></span>  <br/> |<span data-ttu-id="119cd-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="119cd-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="119cd-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="119cd-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="119cd-147">False</span><span class="sxs-lookup"><span data-stu-id="119cd-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="119cd-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="119cd-148">See also</span></span>



- [<span data-ttu-id="119cd-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="119cd-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

