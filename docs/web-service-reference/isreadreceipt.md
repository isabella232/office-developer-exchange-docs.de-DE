---
title: IsReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: Das IsReadReceipt-Element gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: e86a7776bc43204dae9fc92f21d4304255ddb888
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463902"
---
# <a name="isreadreceipt"></a><span data-ttu-id="17839-103">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="17839-103">IsReadReceipt</span></span>

<span data-ttu-id="17839-104">Das **IsReadReceipt** -Element gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="17839-104">The **IsReadReceipt** element indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span> 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 <span data-ttu-id="17839-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="17839-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17839-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17839-106">Attributes and elements</span></span>

<span data-ttu-id="17839-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17839-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17839-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="17839-108">Attributes</span></span>

<span data-ttu-id="17839-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="17839-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17839-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17839-110">Child elements</span></span>

<span data-ttu-id="17839-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="17839-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="17839-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17839-112">Parent elements</span></span>

|<span data-ttu-id="17839-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="17839-113">**Element**</span></span>|<span data-ttu-id="17839-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17839-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17839-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="17839-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="17839-116">Stellt die Bedingungen, die beim erfüllt, wird die Regelaktionen für diese Regel ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="17839-116">Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.</span></span>  <br/> |
|[<span data-ttu-id="17839-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="17839-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="17839-118">Stellt alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="17839-118">Represents all the available rule exception conditions for the Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="17839-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="17839-119">Text value</span></span>

<span data-ttu-id="17839-120">Der Textwert **true** gibt an, dass die Nachricht eine Lesebestätigung sein muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="17839-120">A text value of **true** indicates that the message must be a read receipt in order for the condition or exception to apply.</span></span> <span data-ttu-id="17839-121">Wenn die Nachricht nicht eine Lesebestätigung sein muss, damit die Bedingung oder Ausnahme angewendet wird, ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="17839-121">If the message does not have to be a read receipt for the condition or exception to apply, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17839-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17839-122">Remarks</span></span>

<span data-ttu-id="17839-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="17839-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17839-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="17839-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17839-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="17839-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="17839-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17839-126">Schema Name</span></span>  <br/> |<span data-ttu-id="17839-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="17839-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="17839-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17839-128">Validation File</span></span>  <br/> |<span data-ttu-id="17839-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="17839-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17839-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="17839-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="17839-131">True</span><span class="sxs-lookup"><span data-stu-id="17839-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17839-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17839-132">See also</span></span>



- [<span data-ttu-id="17839-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17839-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

