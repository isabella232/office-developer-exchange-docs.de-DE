---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: Das AssistantPhoneNumbers-Element gibt ein Array von Assistent Rufnummern und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 747835102af28d94d60b763fdbc5b2ea0947d47e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757389"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="b618e-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="b618e-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="b618e-104">Das **AssistantPhoneNumbers** -Element gibt ein Array von Assistent Rufnummern und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="b618e-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="b618e-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="b618e-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b618e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b618e-106">Attributes and elements</span></span>

<span data-ttu-id="b618e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b618e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b618e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b618e-108">Attributes</span></span>

<span data-ttu-id="b618e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b618e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b618e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b618e-110">Child elements</span></span>

|<span data-ttu-id="b618e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b618e-111">**Element**</span></span>|<span data-ttu-id="b618e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b618e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b618e-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="b618e-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="b618e-114">Gibt eine Instanz eines Arrays von Telefonnummern und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="b618e-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b618e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b618e-115">Parent elements</span></span>

|<span data-ttu-id="b618e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b618e-116">**Element**</span></span>|<span data-ttu-id="b618e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b618e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b618e-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="b618e-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="b618e-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b618e-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b618e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b618e-120">Remarks</span></span>

<span data-ttu-id="b618e-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b618e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b618e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b618e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b618e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b618e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b618e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b618e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b618e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b618e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b618e-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="b618e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b618e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b618e-127">Validation File</span></span>  <br/> |<span data-ttu-id="b618e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b618e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b618e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b618e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b618e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b618e-130">See also</span></span>

- [<span data-ttu-id="b618e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b618e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

