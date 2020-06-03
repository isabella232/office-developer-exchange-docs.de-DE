---
title: Element originalrecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalRecipients
api_type:
- schema
ms.assetid: e4af86a5-85af-4239-8055-e29f0acf77c1
description: Das Element OriginalRecipients stellt eine Liste von E-mail-Adressen der Empfänger der ersten Nachricht.
ms.openlocfilehash: 7385b1fd62313ee09c94cd04f3f669215e6cd497
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467179"
---
# <a name="originalrecipients"></a><span data-ttu-id="884db-103">Element originalrecipients</span><span class="sxs-lookup"><span data-stu-id="884db-103">OriginalRecipients</span></span>

<span data-ttu-id="884db-104">Das Element **OriginalRecipients** stellt eine Liste von E-mail-Adressen der Empfänger der ersten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="884db-104">The **OriginalRecipients** element represents a list of e-mail addresses of the first message recipients.</span></span> 
  
```XML
<OriginalRecipients>
   <Address/>
</OriginalRecipients>
```

 <span data-ttu-id="884db-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="884db-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="884db-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="884db-106">Attributes and elements</span></span>

<span data-ttu-id="884db-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="884db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="884db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="884db-108">Attributes</span></span>

<span data-ttu-id="884db-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="884db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="884db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="884db-110">Child elements</span></span>

|<span data-ttu-id="884db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="884db-111">**Element**</span></span>|<span data-ttu-id="884db-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="884db-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="884db-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="884db-114">Eine vollständig aufgelöster E-mail-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="884db-114">Contains a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="884db-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="884db-115">Parent elements</span></span>

|<span data-ttu-id="884db-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="884db-116">**Element**</span></span>|<span data-ttu-id="884db-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884db-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="884db-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="884db-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="884db-119">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="884db-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="884db-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="884db-120">Remarks</span></span>

<span data-ttu-id="884db-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="884db-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="884db-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="884db-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="884db-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="884db-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="884db-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="884db-124">Schema Name</span></span>  <br/> |<span data-ttu-id="884db-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="884db-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="884db-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="884db-126">Validation File</span></span>  <br/> |<span data-ttu-id="884db-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="884db-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="884db-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="884db-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="884db-129">False</span><span class="sxs-lookup"><span data-stu-id="884db-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="884db-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884db-130">See also</span></span>



[<span data-ttu-id="884db-131">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="884db-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="884db-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="884db-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

