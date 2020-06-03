---
title: Aktion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Das Action-Element enthält Informationen, die verwendet werden, um zu bestimmen, ob eine andere Auto Ermittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.
ms.openlocfilehash: f6d542b908948d09020b850b60ca1bdb025dd342
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529693"
---
# <a name="action-pox"></a><span data-ttu-id="c58cc-103">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-103">Action (POX)</span></span>

<span data-ttu-id="c58cc-104">Das **Action** -Element enthält Informationen, die verwendet werden, um zu bestimmen, ob eine andere Auto Ermittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c58cc-104">The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span> 
  
- [<span data-ttu-id="c58cc-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="c58cc-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="c58cc-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="c58cc-108">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-108">Action (POX)</span></span>](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c58cc-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c58cc-109">Attributes and elements</span></span>

<span data-ttu-id="c58cc-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c58cc-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c58cc-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="c58cc-111">Attributes</span></span>

<span data-ttu-id="c58cc-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="c58cc-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c58cc-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c58cc-113">Child elements</span></span>

<span data-ttu-id="c58cc-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="c58cc-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c58cc-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c58cc-115">Parent elements</span></span>

|<span data-ttu-id="c58cc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c58cc-116">**Element**</span></span>|<span data-ttu-id="c58cc-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c58cc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c58cc-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="c58cc-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="c58cc-119">Gibt Kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="c58cc-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c58cc-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="c58cc-120">Text value</span></span>

<span data-ttu-id="c58cc-121">Der Text-Wert gibt an, ob eine andere Auto Ermittlungsanforderung zum Abrufen der Konfigurationsinformationen des Benutzers erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c58cc-121">The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information.</span></span> <span data-ttu-id="c58cc-122">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c58cc-122">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="c58cc-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c58cc-123">**Value**</span></span>|<span data-ttu-id="c58cc-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c58cc-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c58cc-125">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="c58cc-125">redirectUrl</span></span>  <br/> |<span data-ttu-id="c58cc-126">Wenn dieser Wert angegeben ist, gibt das [RedirectUrl (POX)-](redirecturl-pox.md) Element die Client Zugriffsserver-URL an, die in der nachfolgenden Auto Ermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c58cc-126">If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request.</span></span> <span data-ttu-id="c58cc-127">Die Clientanwendung sollte die Umleitung nach 10 Umleitungen beenden.</span><span class="sxs-lookup"><span data-stu-id="c58cc-127">The client application should stop redirecting after 10 redirects.</span></span>  <br/> |
|<span data-ttu-id="c58cc-128">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="c58cc-128">redirectAddr</span></span>  <br/> |<span data-ttu-id="c58cc-129">Wenn dieser Wert angegeben ist, gibt das [RedirectAddr (POX)](redirectaddr-pox.md) -Element die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c58cc-129">If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|<span data-ttu-id="c58cc-130">settings</span><span class="sxs-lookup"><span data-stu-id="c58cc-130">settings</span></span>  <br/> |<span data-ttu-id="c58cc-131">Wenn dieser Wert angegeben ist, enthält die Auto Ermittlungs Antworteinstellungen, die zum Konfigurieren des Kontos verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c58cc-131">If this value is specified, the Autodiscover response contains settings that are used to configure the account.</span></span> <span data-ttu-id="c58cc-132">Die meisten Einstellungen finden Sie im [Protokoll (POX)](protocol-pox.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="c58cc-132">Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c58cc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c58cc-133">See also</span></span>

- [<span data-ttu-id="c58cc-134">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="c58cc-134">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

