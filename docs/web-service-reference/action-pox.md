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
description: Das Action-Element enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben.
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758383"
---
# <a name="action-pox"></a><span data-ttu-id="21742-103">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-103">Action (POX)</span></span>

<span data-ttu-id="21742-104">Das **Action** -Element enthält Informationen, die verwendet wird, um festzustellen, ob eine andere autoermittlungsanforderung erforderlich ist, um die Informationen der Benutzerkonfiguration zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="21742-104">The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span> 
  
- [<span data-ttu-id="21742-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="21742-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="21742-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="21742-108">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-108">Action (POX)</span></span>](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="21742-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21742-109">Attributes and elements</span></span>

<span data-ttu-id="21742-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21742-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21742-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="21742-111">Attributes</span></span>

<span data-ttu-id="21742-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="21742-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21742-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21742-113">Child elements</span></span>

<span data-ttu-id="21742-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="21742-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21742-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21742-115">Parent elements</span></span>

|<span data-ttu-id="21742-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="21742-116">**Element**</span></span>|<span data-ttu-id="21742-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21742-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21742-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="21742-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="21742-119">Gibt die kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="21742-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21742-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="21742-120">Text value</span></span>

<span data-ttu-id="21742-121">Der Textwert der angibt, ob einer anderen autoermittlungsanforderung erforderlich sind, um die Konfigurationsinformationen des Benutzers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21742-121">The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information.</span></span> <span data-ttu-id="21742-122">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="21742-122">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="21742-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="21742-123">**Value**</span></span>|<span data-ttu-id="21742-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21742-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21742-125">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="21742-125">redirectUrl</span></span>  <br/> |<span data-ttu-id="21742-126">Wenn dieser Wert angegeben ist, wird das Element [RedirectUrl (POX)](redirecturl-pox.md) die Clientzugriffs-Server-URL in der nachfolgenden Anforderung der AutoErmittlung verwendet werden angeben.</span><span class="sxs-lookup"><span data-stu-id="21742-126">If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request.</span></span> <span data-ttu-id="21742-127">Die Clientanwendung sollte beenden umleiten nach 10 umleitungen zulässig.</span><span class="sxs-lookup"><span data-stu-id="21742-127">The client application should stop redirecting after 10 redirects.</span></span>  <br/> |
|<span data-ttu-id="21742-128">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="21742-128">redirectAddr</span></span>  <br/> |<span data-ttu-id="21742-129">Wenn dieser Wert angegeben ist, wird das Element [RedirectAddr (POX)](redirectaddr-pox.md) die e-Mail-Adresse angeben, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21742-129">If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|<span data-ttu-id="21742-130">settings</span><span class="sxs-lookup"><span data-stu-id="21742-130">settings</span></span>  <br/> |<span data-ttu-id="21742-131">Wenn dieser Wert angegeben wird, enthält die Antwort der AutoErmittlung Einstellungen, mit denen das Konto konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="21742-131">If this value is specified, the Autodiscover response contains settings that are used to configure the account.</span></span> <span data-ttu-id="21742-132">Die meisten Einstellungen werden im [Protokoll (POX)](protocol-pox.md) -Element gefunden.</span><span class="sxs-lookup"><span data-stu-id="21742-132">Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21742-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21742-133">See also</span></span>

- [<span data-ttu-id="21742-134">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="21742-134">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

