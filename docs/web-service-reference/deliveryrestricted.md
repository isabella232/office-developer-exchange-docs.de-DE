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
description: Das DeliveryRestricted-Element gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.
ms.openlocfilehash: ba1c6e00b93c9e442a427fe98a5e15bf5fe1effd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757950"
---
# <a name="deliveryrestricted"></a><span data-ttu-id="1256b-103">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="1256b-103">DeliveryRestricted</span></span>

<span data-ttu-id="1256b-104">Das **DeliveryRestricted** -Element gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1256b-104">The **DeliveryRestricted** element indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 <span data-ttu-id="1256b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1256b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1256b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1256b-106">Attributes and elements</span></span>

<span data-ttu-id="1256b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1256b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1256b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1256b-108">Attributes</span></span>

<span data-ttu-id="1256b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1256b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1256b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1256b-110">Child elements</span></span>

<span data-ttu-id="1256b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1256b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1256b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1256b-112">Parent elements</span></span>

|<span data-ttu-id="1256b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1256b-113">**Element**</span></span>|<span data-ttu-id="1256b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1256b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1256b-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="1256b-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="1256b-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="1256b-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1256b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1256b-117">Text value</span></span>

<span data-ttu-id="1256b-118">Der Textwert der dieses Element ist **true** , wenn die Zustellung Einschränkungen des Absenders der Nachricht verhindern Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1256b-118">The text value of this element is **true** if delivery restrictions will prevent the sender's message from reaching the recipient.</span></span> <span data-ttu-id="1256b-119">Der Wert ist **false** , wenn Delivery Restrictions, nicht verhindert, dass der Nachricht des Absenders Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1256b-119">The value is **false** if delivery restrictions will not prevent the sender's message from reaching the recipient.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1256b-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1256b-120">Remarks</span></span>

<span data-ttu-id="1256b-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1256b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1256b-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1256b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1256b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1256b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1256b-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1256b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1256b-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1256b-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="1256b-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1256b-126">Validation File</span></span>  <br/> |<span data-ttu-id="1256b-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1256b-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1256b-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1256b-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="1256b-129">False</span><span class="sxs-lookup"><span data-stu-id="1256b-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1256b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1256b-130">See also</span></span>

- [<span data-ttu-id="1256b-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1256b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

