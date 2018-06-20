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
description: Das MaxRecipientsPerGetMailTipsRequest-Element gibt die maximale Anzahl von Empfängern, die für den Betrieb GetMailTips übergeben werden kann.
ms.openlocfilehash: 4c873fe534582e582bf5b1c1d5fd2789616e056a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830386"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="83570-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="83570-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="83570-104">Das **MaxRecipientsPerGetMailTipsRequest** -Element gibt die maximale Anzahl von Empfängern, die an den [GetMailTips Vorgang](getmailtips-operation.md)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="83570-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="83570-105">**int**</span><span class="sxs-lookup"><span data-stu-id="83570-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83570-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83570-106">Attributes and elements</span></span>

<span data-ttu-id="83570-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83570-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83570-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83570-108">Attributes</span></span>

<span data-ttu-id="83570-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83570-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83570-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83570-110">Child elements</span></span>

<span data-ttu-id="83570-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="83570-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83570-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83570-112">Parent elements</span></span>

|<span data-ttu-id="83570-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83570-113">**Element**</span></span>|<span data-ttu-id="83570-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83570-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83570-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="83570-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="83570-116">Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="83570-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83570-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="83570-117">Text value</span></span>

<span data-ttu-id="83570-118">Der Textwert ist eine ganze Zahl, die die maximale Anzahl von Empfängern darstellt, um den [Vorgang GetMailTips](getmailtips-operation.md)übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="83570-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83570-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83570-119">Remarks</span></span>

<span data-ttu-id="83570-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83570-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83570-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83570-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83570-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="83570-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83570-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83570-123">Schema Name</span></span>  <br/> |<span data-ttu-id="83570-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83570-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="83570-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83570-125">Validation File</span></span>  <br/> |<span data-ttu-id="83570-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83570-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83570-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83570-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="83570-128">False</span><span class="sxs-lookup"><span data-stu-id="83570-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83570-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83570-129">See also</span></span>



[<span data-ttu-id="83570-130">GetMailTips-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83570-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="83570-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83570-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

