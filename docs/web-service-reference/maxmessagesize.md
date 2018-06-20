---
title: MaxMessageSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxMessageSize
api_type:
- schema
ms.assetid: bb98ac72-9409-4332-81bb-ee3bebb9a00e
description: Das Element MaxMessageSize stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.
ms.openlocfilehash: 13a5679a03420655356269a7e8b5e22950724164
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830383"
---
# <a name="maxmessagesize"></a><span data-ttu-id="479c3-103">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="479c3-103">MaxMessageSize</span></span>

<span data-ttu-id="479c3-104">Das Element **MaxMessageSize** stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="479c3-104">The **MaxMessageSize** element represents the maximum message size a recipient can accept.</span></span> 
  
```XML
<MaxMessageSize/>
```

 <span data-ttu-id="479c3-105">**int**</span><span class="sxs-lookup"><span data-stu-id="479c3-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="479c3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="479c3-106">Attributes and elements</span></span>

<span data-ttu-id="479c3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="479c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="479c3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="479c3-108">Attributes</span></span>

<span data-ttu-id="479c3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="479c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="479c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="479c3-110">Child elements</span></span>

<span data-ttu-id="479c3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="479c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="479c3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="479c3-112">Parent elements</span></span>

|<span data-ttu-id="479c3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="479c3-113">**Element**</span></span>|<span data-ttu-id="479c3-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="479c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="479c3-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="479c3-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="479c3-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="479c3-116">Represents values for various types of mail tips.</span></span>  <br/> |
|[<span data-ttu-id="479c3-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="479c3-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="479c3-118">Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="479c3-118">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="479c3-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="479c3-119">Text value</span></span>

<span data-ttu-id="479c3-120">Der Text ist eine ganze Zahl, die die maximale Größe eines Empfängers darstellt akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="479c3-120">The text value is an integer that represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="479c3-121">Dieser Wert kann in Kilobyte oder Megabyte gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="479c3-121">This value can be measured in kilobytes or megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="479c3-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="479c3-122">Remarks</span></span>

<span data-ttu-id="479c3-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="479c3-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="479c3-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="479c3-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="479c3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="479c3-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="479c3-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="479c3-126">Schema Name</span></span>  <br/> |<span data-ttu-id="479c3-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="479c3-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="479c3-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="479c3-128">Validation File</span></span>  <br/> |<span data-ttu-id="479c3-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="479c3-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="479c3-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="479c3-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="479c3-131">False</span><span class="sxs-lookup"><span data-stu-id="479c3-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="479c3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="479c3-132">See also</span></span>



- [<span data-ttu-id="479c3-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="479c3-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

