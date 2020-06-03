---
title: Konto (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Das Account-Element gibt Kontoeinstellungen für den Benutzer an oder enthält Fehlerantworten.
ms.openlocfilehash: ffd8ebe4b7bd9d4b3f6a9b42fc557ac6189a068d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462318"
---
# <a name="account-pox"></a><span data-ttu-id="fa2ee-103">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-103">Account (POX)</span></span>

<span data-ttu-id="fa2ee-104">Das **Account** -Element gibt Kontoeinstellungen für den Benutzer an oder enthält Fehlerantworten.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="fa2ee-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
- [<span data-ttu-id="fa2ee-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="fa2ee-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-107">Account (POX)</span></span>](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fa2ee-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa2ee-108">Attributes and elements</span></span>

<span data-ttu-id="fa2ee-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa2ee-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa2ee-110">Attributes</span></span>

<span data-ttu-id="fa2ee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa2ee-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa2ee-112">Child elements</span></span>

|<span data-ttu-id="fa2ee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa2ee-113">**Element**</span></span>|<span data-ttu-id="fa2ee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa2ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa2ee-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="fa2ee-116">Stellt den Kontotyp dar.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-117">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="fa2ee-118">Enthält Informationen, die verwendet werden, um zu bestimmen, ob eine andere Auto Ermittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-119">Microsoft Online (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="fa2ee-120">Enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil von Office 365 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="fa2ee-122">Enthält die URL des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="fa2ee-124">Gibt die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-125">Bild (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="fa2ee-126">Enthält den Pfad eines Bilds, das zum Branding der Konfigurationsumgebung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="fa2ee-128">Enthält die URL der Startseite des Internetdienstanbieters (Internet Service Provider, ISP).</span><span class="sxs-lookup"><span data-stu-id="fa2ee-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-129">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="fa2ee-130">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="fa2ee-132">Enthält Informationen, die Clients verwenden können, um eine Auto Ermittlungsanforderung zu senden, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="fa2ee-133">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="fa2ee-134">Enthält eine AutoErmittlung-Fehlerantwort.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa2ee-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa2ee-135">Parent elements</span></span>

|<span data-ttu-id="fa2ee-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa2ee-136">**Element**</span></span>|<span data-ttu-id="fa2ee-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa2ee-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa2ee-138">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="fa2ee-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="fa2ee-139">Enthält die Antwort des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="fa2ee-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa2ee-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa2ee-140">See also</span></span>

- [<span data-ttu-id="fa2ee-141">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="fa2ee-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

