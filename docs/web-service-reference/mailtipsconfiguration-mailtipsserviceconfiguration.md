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
description: Das MailTipsConfiguration-Element enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.
ms.openlocfilehash: 9128ee99545066899c3b27b624f10a9f1bd36c9d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467788"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="658a5-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="658a5-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="658a5-104">Das **MailTipsConfiguration** -Element enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="658a5-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
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

 <span data-ttu-id="658a5-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="658a5-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="658a5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="658a5-106">Attributes and elements</span></span>

<span data-ttu-id="658a5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="658a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="658a5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="658a5-108">Attributes</span></span>

<span data-ttu-id="658a5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="658a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="658a5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="658a5-110">Child elements</span></span>

|<span data-ttu-id="658a5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="658a5-111">**Element**</span></span>|<span data-ttu-id="658a5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="658a5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="658a5-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="658a5-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="658a5-114">Gibt an, ob der e-Mail-Spitzen Dienst verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="658a5-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="658a5-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="658a5-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="658a5-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="658a5-117">Gibt die maximale Anzahl von Empfängern an, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="658a5-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="658a5-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="658a5-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="658a5-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="658a5-120">Stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="658a5-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="658a5-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="658a5-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="658a5-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="658a5-123">Stellt den Schwellenwert für hohe Benutzergruppen für einen Client dar.</span><span class="sxs-lookup"><span data-stu-id="658a5-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="658a5-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="658a5-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="658a5-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="658a5-126">Gibt an, ob Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="658a5-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="658a5-127">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="658a5-128">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="658a5-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="658a5-129">Gibt die Liste der internen SMTP-Domänen der Organisation an.</span><span class="sxs-lookup"><span data-stu-id="658a5-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="658a5-130">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="658a5-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="658a5-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="658a5-131">Parent elements</span></span>

|<span data-ttu-id="658a5-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="658a5-132">**Element**</span></span>|<span data-ttu-id="658a5-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="658a5-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="658a5-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="658a5-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="658a5-135">Enthält Dienst Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="658a5-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="658a5-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="658a5-136">Text value</span></span>

<span data-ttu-id="658a5-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="658a5-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="658a5-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="658a5-138">Remarks</span></span>

<span data-ttu-id="658a5-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="658a5-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="658a5-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="658a5-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="658a5-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="658a5-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="658a5-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="658a5-142">Schema Name</span></span>  <br/> |<span data-ttu-id="658a5-143">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="658a5-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="658a5-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="658a5-144">Validation File</span></span>  <br/> |<span data-ttu-id="658a5-145">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="658a5-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="658a5-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="658a5-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="658a5-147">False</span><span class="sxs-lookup"><span data-stu-id="658a5-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="658a5-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="658a5-148">See also</span></span>



- [<span data-ttu-id="658a5-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="658a5-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

