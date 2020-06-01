---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: Das DeliveryRestricted-Element gibt an, ob zustellungseinschränkungen verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann.
ms.openlocfilehash: 58fc85873326179d7745db4ba7d4854a76ced6a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462689"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="89799-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="89799-103">DeliveryRestricted</span></span>

<span data-ttu-id="89799-104">Das **DeliveryRestricted** -Element gibt an, ob zustellungseinschränkungen verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="89799-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="89799-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="89799-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89799-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="89799-106">Attributes and elements</span></span>

<span data-ttu-id="89799-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="89799-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89799-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="89799-108">Attributes</span></span>

<span data-ttu-id="89799-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="89799-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89799-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89799-110">Child elements</span></span>

<span data-ttu-id="89799-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="89799-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89799-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89799-112">Parent elements</span></span>

|<span data-ttu-id="89799-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="89799-113">**Element**</span></span>|<span data-ttu-id="89799-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="89799-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89799-115">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="89799-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="89799-116">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="89799-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89799-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="89799-117">Text value</span></span>

<span data-ttu-id="89799-118">Der Textwert dieses Elements ist **true** , wenn zustellungseinschränkungen verhindert werden, dass die Nachricht des Absenders den Empfänger erreicht.</span><span class="sxs-lookup"><span data-stu-id="89799-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="89799-119">Der Wert ist **false** , wenn zustellungseinschränkungen nicht verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="89799-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89799-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89799-120">Remarks</span></span>

<span data-ttu-id="89799-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="89799-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89799-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="89799-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89799-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="89799-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89799-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="89799-124">Schema Name</span></span>  <br/> |<span data-ttu-id="89799-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="89799-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="89799-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="89799-126">Validation File</span></span>  <br/> |<span data-ttu-id="89799-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89799-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89799-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="89799-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="89799-129">False</span><span class="sxs-lookup"><span data-stu-id="89799-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89799-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89799-130">See also</span></span>

- [<span data-ttu-id="89799-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="89799-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

