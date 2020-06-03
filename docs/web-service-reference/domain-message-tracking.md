---
title: Domäne (Nachrichtenverfolgung)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 4e8e9efa-8885-4ca5-bf90-424e63768dc3
description: Das Domain-Element stellt die Domäne dar, nach der gesucht werden soll.
ms.openlocfilehash: 77da9028766881b9bc633e1b3318cd4d70c6b72f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457025"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="5a884-103">Domäne (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="5a884-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="5a884-104">Das **Domain** -Element stellt die Domäne dar, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a884-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="5a884-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="5a884-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a884-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a884-106">Attributes and elements</span></span>

<span data-ttu-id="5a884-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a884-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a884-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a884-108">Attributes</span></span>

<span data-ttu-id="5a884-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a884-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a884-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a884-110">Child elements</span></span>

<span data-ttu-id="5a884-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a884-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a884-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a884-112">Parent elements</span></span>

|<span data-ttu-id="5a884-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a884-113">**Element**</span></span>|<span data-ttu-id="5a884-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a884-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a884-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5a884-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="5a884-116">Enthält die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="5a884-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a884-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5a884-117">Text value</span></span>

<span data-ttu-id="5a884-118">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a884-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a884-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a884-119">Remarks</span></span>

<span data-ttu-id="5a884-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5a884-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a884-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5a884-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a884-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a884-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5a884-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a884-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5a884-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5a884-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5a884-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a884-125">Validation File</span></span>  <br/> |<span data-ttu-id="5a884-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5a884-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5a884-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a884-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a884-128">False</span><span class="sxs-lookup"><span data-stu-id="5a884-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a884-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a884-129">See also</span></span>

- [<span data-ttu-id="5a884-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5a884-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

