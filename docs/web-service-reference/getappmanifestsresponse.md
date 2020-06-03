---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: Das GetAppManifestsResponse-Element definiert die Antwort für eine GetAppManifests-Vorgangsanforderung.
ms.openlocfilehash: a01f6265d6d534e2f7868b17acf19f0f5d52a01f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462964"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="7ce60-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="7ce60-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="7ce60-104">Das **GetAppManifestsResponse** -Element definiert die Antwort für eine **GetAppManifests** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="7ce60-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Manifests/>
</GetAppManifestsResponse>
```

```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Apps/>
</GetAppManifestsResponse>
```

<span data-ttu-id="7ce60-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="7ce60-105">**GetAppManifestsResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7ce60-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7ce60-106">Attributes and elements</span></span>

<span data-ttu-id="7ce60-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7ce60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ce60-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7ce60-108">Attributes</span></span>

<span data-ttu-id="7ce60-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7ce60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ce60-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7ce60-110">Child elements</span></span>

<span data-ttu-id="7ce60-111">[Response Code](responsecode.md)  |  [Manifeste](manifests.md)  |  [Apps](apps.md)</span><span class="sxs-lookup"><span data-stu-id="7ce60-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ce60-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7ce60-112">Parent elements</span></span>

<span data-ttu-id="7ce60-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7ce60-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ce60-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ce60-114">Remarks</span></span>

<span data-ttu-id="7ce60-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7ce60-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7ce60-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7ce60-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ce60-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7ce60-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ce60-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ce60-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7ce60-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7ce60-119">Schema Name</span></span>  <br/> |<span data-ttu-id="7ce60-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7ce60-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="7ce60-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7ce60-121">Validation File</span></span>  <br/> |<span data-ttu-id="7ce60-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7ce60-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7ce60-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7ce60-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="7ce60-124">False</span><span class="sxs-lookup"><span data-stu-id="7ce60-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ce60-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ce60-125">See also</span></span>

- [<span data-ttu-id="7ce60-126">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7ce60-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

