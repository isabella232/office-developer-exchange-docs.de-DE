---
title: IsMeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeetingResponse
api_type:
- schema
ms.assetid: 85090943-81c6-4fbe-a2db-007dced6a4cf
description: Das IsMeetngResponsequest-Element gibt an, ob eingehende Nachrichten eine Antwort auf Besprechungsanfrage in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.
ms.openlocfilehash: 9040859452a48916a969b6d8e4e370b5785c1c1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830053"
---
# <a name="ismeetingresponse"></a><span data-ttu-id="fba71-103">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="fba71-103">IsMeetingResponse</span></span>

<span data-ttu-id="fba71-104">Das **IsMeetngResponsequest** -Element gibt an, ob eingehende Nachrichten eine Antwort auf Besprechungsanfrage in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fba71-104">The **IsMeetngResponsequest** element indicates whether incoming messages must be a meeting response in order for the condition or exception to apply.</span></span> 
  
```XML
<IsMeetingResponse/>true | false</IsMeetingResponse>
```

 <span data-ttu-id="fba71-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fba71-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fba71-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fba71-106">Attributes and elements</span></span>

<span data-ttu-id="fba71-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fba71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fba71-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fba71-108">Attributes</span></span>

<span data-ttu-id="fba71-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fba71-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fba71-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fba71-110">Child elements</span></span>

<span data-ttu-id="fba71-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fba71-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fba71-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fba71-112">Parent elements</span></span>

|<span data-ttu-id="fba71-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fba71-113">**Element**</span></span>|<span data-ttu-id="fba71-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fba71-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fba71-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="fba71-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="fba71-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fba71-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="fba71-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="fba71-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="fba71-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="fba71-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fba71-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="fba71-119">Text value</span></span>

<span data-ttu-id="fba71-120">Der Textwert **true** gibt an, dass die Nachricht eine Antwort auf Besprechungsanfrage in Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fba71-120">A text value of **true** indicates that the message must be a meeting response in order for the condition or exception to apply.</span></span> <span data-ttu-id="fba71-121">Der Textwert **false** gibt an, dass die Nachricht keine Antwort auf Besprechungsanfrage in Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fba71-121">A text value of **false** indicates that the message must not be a meeting response in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fba71-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fba71-122">Remarks</span></span>

<span data-ttu-id="fba71-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fba71-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fba71-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fba71-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fba71-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fba71-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fba71-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fba71-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fba71-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fba71-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fba71-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fba71-128">Validation File</span></span>  <br/> |<span data-ttu-id="fba71-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fba71-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fba71-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fba71-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fba71-131">True</span><span class="sxs-lookup"><span data-stu-id="fba71-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fba71-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fba71-132">See also</span></span>



- [<span data-ttu-id="fba71-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fba71-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

