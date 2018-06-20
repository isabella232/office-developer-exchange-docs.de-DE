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
description: Das Konto-Element gibt Konten-Einstellungen für den Benutzer oder Fehlerantworten enthält.
ms.openlocfilehash: 88911aad41816f7cefbffef151e066fe5d4da192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758379"
---
# <a name="account-pox"></a><span data-ttu-id="3a5d2-103">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-103">Account (POX)</span></span>

<span data-ttu-id="3a5d2-104">Das **Konto** -Element gibt Konten-Einstellungen für den Benutzer oder Fehlerantworten enthält.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="3a5d2-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="3a5d2-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="3a5d2-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-107">Account (POX)</span></span>](account-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="3a5d2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3a5d2-108">Attributes and elements</span></span>

<span data-ttu-id="3a5d2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a5d2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3a5d2-110">Attributes</span></span>

<span data-ttu-id="3a5d2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a5d2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a5d2-112">Child elements</span></span>

|<span data-ttu-id="3a5d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a5d2-113">**Element**</span></span>|<span data-ttu-id="3a5d2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a5d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5d2-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="3a5d2-116">Stellt die Kontenart an.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-117">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="3a5d2-118">Enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-119">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="3a5d2-120">Enthält einen Wert, der angibt, ob das Postfach des Benutzers im Exchange Online gehostet wird oder Exchange Online als Teil von Office 365.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="3a5d2-122">Enthält die URL des Computers, der Exchange-Server ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="3a5d2-124">Gibt die e-Mail-Adresse, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-125">Bild (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="3a5d2-126">Enthält den Pfad eines Bilds, das verwendet wird, um die Konfiguration Erfahrung mit Branding versehen.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="3a5d2-128">Enthält die URL der Startseite des Internet-Dienstanbieters (ISP).</span><span class="sxs-lookup"><span data-stu-id="3a5d2-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-129">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="3a5d2-130">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="3a5d2-132">Enthält Informationen, mit denen Clients eine Anforderung der AutoErmittlung zum Ermitteln von Öffentliche Ordner-Informationen für den Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="3a5d2-133">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="3a5d2-134">Enthält eine Fehlerantwort AutoErmittlung an.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a5d2-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a5d2-135">Parent elements</span></span>

|<span data-ttu-id="3a5d2-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a5d2-136">**Element**</span></span>|<span data-ttu-id="3a5d2-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a5d2-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5d2-138">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="3a5d2-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="3a5d2-139">Enthält die Antwort vom AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="3a5d2-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a5d2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a5d2-140">See also</span></span>

- [<span data-ttu-id="3a5d2-141">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="3a5d2-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

