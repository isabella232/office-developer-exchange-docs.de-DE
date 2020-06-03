---
title: InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc2ca69e-eea7-4334-b046-ec0b04d8f8c6
description: Das InstallApp-Element gibt die Anforderung an, eine APP zu installieren.
ms.openlocfilehash: 003a72507813677484b2d6ee75f8ff577df169e3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468005"
---
# <a name="installapp"></a><span data-ttu-id="4ef00-103">InstallApp</span><span class="sxs-lookup"><span data-stu-id="4ef00-103">InstallApp</span></span>

<span data-ttu-id="4ef00-104">Das **InstallApp** -Element gibt die Anforderung an, eine APP zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4ef00-104">The **InstallApp** element specifies the request to install an app.</span></span> 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 <span data-ttu-id="4ef00-105">**InstallAppType**</span><span class="sxs-lookup"><span data-stu-id="4ef00-105">**InstallAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ef00-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef00-106">Attributes and elements</span></span>

<span data-ttu-id="4ef00-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ef00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ef00-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ef00-108">Attributes</span></span>

<span data-ttu-id="4ef00-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ef00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ef00-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef00-110">Child elements</span></span>

|<span data-ttu-id="4ef00-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ef00-111">**Element**</span></span>|<span data-ttu-id="4ef00-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ef00-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ef00-113">Manifest</span><span class="sxs-lookup"><span data-stu-id="4ef00-113">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="4ef00-114">Enthält die Base64-codierte App-Manifestdatei.</span><span class="sxs-lookup"><span data-stu-id="4ef00-114">Contains the base64-encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ef00-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef00-115">Parent elements</span></span>

<span data-ttu-id="4ef00-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ef00-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ef00-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ef00-117">Remarks</span></span>

<span data-ttu-id="4ef00-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4ef00-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4ef00-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4ef00-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ef00-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4ef00-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ef00-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ef00-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ef00-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ef00-122">Schema Name</span></span>  <br/> |<span data-ttu-id="4ef00-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4ef00-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="4ef00-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ef00-124">Validation File</span></span>  <br/> |<span data-ttu-id="4ef00-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4ef00-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ef00-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4ef00-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4ef00-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ef00-127">See also</span></span>



- [<span data-ttu-id="4ef00-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ef00-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

