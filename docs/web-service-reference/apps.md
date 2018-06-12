---
title: Apps
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6f0a2ca-22dd-4789-9eed-f0c1ec9036c4
description: Das Apps-Element enthält Informationen über alle XML-Manifestdateien für apps in einem Postfach installiert.
ms.openlocfilehash: 81b0cb76b02fcc9145f6d70eff12a0a0ac0ad51f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757368"
---
# <a name="apps"></a><span data-ttu-id="5dd2b-103">Apps</span><span class="sxs-lookup"><span data-stu-id="5dd2b-103">Apps</span></span>

<span data-ttu-id="5dd2b-104">Das **Apps** -Element enthält Informationen über alle XML-Manifestdateien für apps in einem Postfach installiert.</span><span class="sxs-lookup"><span data-stu-id="5dd2b-104">The **Apps** element contains information about all the XML manifest files for apps installed in a mailbox.</span></span> 
  
```XML
<Apps>
    <App/>
</Apps>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5dd2b-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5dd2b-105">Attributes and elements</span></span>

<span data-ttu-id="5dd2b-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5dd2b-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dd2b-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="5dd2b-107">Attributes</span></span>

<span data-ttu-id="5dd2b-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="5dd2b-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5dd2b-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5dd2b-109">Child elements</span></span>

[<span data-ttu-id="5dd2b-110">App</span><span class="sxs-lookup"><span data-stu-id="5dd2b-110">App</span></span>](app.md)
  
### <a name="parent-elements"></a><span data-ttu-id="5dd2b-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5dd2b-111">Parent elements</span></span>

[<span data-ttu-id="5dd2b-112">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="5dd2b-112">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="5dd2b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5dd2b-113">Remarks</span></span>

<span data-ttu-id="5dd2b-114">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5dd2b-114">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="5dd2b-115">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5dd2b-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dd2b-116">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5dd2b-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dd2b-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dd2b-117">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5dd2b-118">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5dd2b-118">Schema Name</span></span>  <br/> |<span data-ttu-id="5dd2b-119">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5dd2b-119">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5dd2b-120">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5dd2b-120">Validation File</span></span>  <br/> |<span data-ttu-id="5dd2b-121">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="5dd2b-121">Not applicable</span></span>  <br/> |
|<span data-ttu-id="5dd2b-122">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5dd2b-122">Can be Empty</span></span>  <br/> |<span data-ttu-id="5dd2b-123">False</span><span class="sxs-lookup"><span data-stu-id="5dd2b-123">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5dd2b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd2b-124">See also</span></span>

- [<span data-ttu-id="5dd2b-125">App</span><span class="sxs-lookup"><span data-stu-id="5dd2b-125">App</span></span>](app.md)
- [<span data-ttu-id="5dd2b-126">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="5dd2b-126">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
- [<span data-ttu-id="5dd2b-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5dd2b-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
