---
title: App
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92b776b5-fec6-4443-a606-51ccb06f7afd
description: Das App-Element enthält Informationen über eine XML-Manifestdatei für eine Mail-app, die in einem Postfach installiert ist.
ms.openlocfilehash: c63bbbf6eb3bf718b2cf81e67d9ec978b3bc5f8d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757272"
---
# <a name="app"></a><span data-ttu-id="005a4-103">App</span><span class="sxs-lookup"><span data-stu-id="005a4-103">App</span></span>

<span data-ttu-id="005a4-104">Das **App** -Element enthält Informationen über eine XML-Manifestdatei für eine Mail-app, die in einem Postfach installiert ist.</span><span class="sxs-lookup"><span data-stu-id="005a4-104">The **App** element contains information about an XML manifest file for a mail app that is installed in a mailbox.</span></span> 
  
```XML
<App>
    <Metadata/>
    <Manifest/>
</App>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="005a4-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="005a4-105">Attributes and elements</span></span>

<span data-ttu-id="005a4-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="005a4-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="005a4-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="005a4-107">Attributes</span></span>

<span data-ttu-id="005a4-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="005a4-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="005a4-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="005a4-109">Child elements</span></span>

<span data-ttu-id="005a4-110">[Metadaten](metadata-ex15websvcsotherref.md) | [Manifest](manifest.md)</span><span class="sxs-lookup"><span data-stu-id="005a4-110">[Metadata](metadata-ex15websvcsotherref.md) | [Manifest](manifest.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="005a4-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="005a4-111">Parent elements</span></span>

[<span data-ttu-id="005a4-112">Apps</span><span class="sxs-lookup"><span data-stu-id="005a4-112">Apps</span></span>](apps.md)
  
## <a name="remarks"></a><span data-ttu-id="005a4-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="005a4-113">Remarks</span></span>

<span data-ttu-id="005a4-114">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="005a4-114">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="005a4-115">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="005a4-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="005a4-116">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="005a4-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="005a4-117">Namespace</span><span class="sxs-lookup"><span data-stu-id="005a4-117">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="005a4-118">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="005a4-118">Schema Name</span></span>  <br/> |<span data-ttu-id="005a4-119">Schematypen</span><span class="sxs-lookup"><span data-stu-id="005a4-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="005a4-120">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="005a4-120">Validation File</span></span>  <br/> |<span data-ttu-id="005a4-121">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="005a4-121">Not applicable</span></span>  <br/> |
|<span data-ttu-id="005a4-122">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="005a4-122">Can be Empty</span></span>  <br/> |<span data-ttu-id="005a4-123">False</span><span class="sxs-lookup"><span data-stu-id="005a4-123">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="005a4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="005a4-124">See also</span></span>

- [<span data-ttu-id="005a4-125">Apps</span><span class="sxs-lookup"><span data-stu-id="005a4-125">Apps</span></span>](apps.md)
- [<span data-ttu-id="005a4-126">Metadaten</span><span class="sxs-lookup"><span data-stu-id="005a4-126">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="005a4-127">Manifest</span><span class="sxs-lookup"><span data-stu-id="005a4-127">Manifest</span></span>](manifest.md)
- [<span data-ttu-id="005a4-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="005a4-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

