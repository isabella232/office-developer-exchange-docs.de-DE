---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: Das MaxRecipientsPerGetMailTipsRequest-Element gibt die maximale Anzahl von Empfängern an, die an den GetMailTips-Vorgang übergeben werden können.
ms.openlocfilehash: cec343182b364fce040d5e32928cbeb569a22124
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468404"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="30f51-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="30f51-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="30f51-104">Das **MaxRecipientsPerGetMailTipsRequest** -Element gibt die maximale Anzahl von Empfängern an, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="30f51-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="30f51-105">**int**</span><span class="sxs-lookup"><span data-stu-id="30f51-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30f51-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="30f51-106">Attributes and elements</span></span>

<span data-ttu-id="30f51-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="30f51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30f51-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="30f51-108">Attributes</span></span>

<span data-ttu-id="30f51-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="30f51-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30f51-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30f51-110">Child elements</span></span>

<span data-ttu-id="30f51-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="30f51-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30f51-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30f51-112">Parent elements</span></span>

|<span data-ttu-id="30f51-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="30f51-113">**Element**</span></span>|<span data-ttu-id="30f51-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30f51-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30f51-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="30f51-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="30f51-116">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="30f51-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30f51-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="30f51-117">Text value</span></span>

<span data-ttu-id="30f51-118">Der Textwert ist ein Integer-Wert, der die maximale Anzahl von Empfängern darstellt, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="30f51-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30f51-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30f51-119">Remarks</span></span>

<span data-ttu-id="30f51-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="30f51-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30f51-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="30f51-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30f51-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="30f51-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30f51-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="30f51-123">Schema Name</span></span>  <br/> |<span data-ttu-id="30f51-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="30f51-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="30f51-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="30f51-125">Validation File</span></span>  <br/> |<span data-ttu-id="30f51-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30f51-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30f51-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="30f51-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="30f51-128">False</span><span class="sxs-lookup"><span data-stu-id="30f51-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30f51-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30f51-129">See also</span></span>



[<span data-ttu-id="30f51-130">GetMailTips-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30f51-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="30f51-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="30f51-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

