---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: Das AssistantPhoneNumbers-Element gibt ein Array von Telefonnummern für den Assistenten und die Bezeichner ihrer Quell Zuordnungen für die zugeordnete Rolle an.
ms.openlocfilehash: a72c8d646750b5d7cf9ebca13a51f4df84bf7bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464483"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="360a6-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="360a6-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="360a6-104">Das **AssistantPhoneNumbers** -Element gibt ein Array von Telefonnummern für den Assistenten und die Bezeichner ihrer Quell Zuordnungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="360a6-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="360a6-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="360a6-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="360a6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="360a6-106">Attributes and elements</span></span>

<span data-ttu-id="360a6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="360a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="360a6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="360a6-108">Attributes</span></span>

<span data-ttu-id="360a6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="360a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="360a6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="360a6-110">Child elements</span></span>

|<span data-ttu-id="360a6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="360a6-111">**Element**</span></span>|<span data-ttu-id="360a6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="360a6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="360a6-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="360a6-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="360a6-114">Gibt eine Instanz eines Arrays von Telefonnummern und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="360a6-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="360a6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="360a6-115">Parent elements</span></span>

|<span data-ttu-id="360a6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="360a6-116">**Element**</span></span>|<span data-ttu-id="360a6-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="360a6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="360a6-118">Persona</span><span class="sxs-lookup"><span data-stu-id="360a6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="360a6-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="360a6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="360a6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="360a6-120">Remarks</span></span>

<span data-ttu-id="360a6-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="360a6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="360a6-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="360a6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="360a6-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="360a6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="360a6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="360a6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="360a6-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="360a6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="360a6-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="360a6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="360a6-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="360a6-127">Validation File</span></span>  <br/> |<span data-ttu-id="360a6-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="360a6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="360a6-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="360a6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="360a6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="360a6-130">See also</span></span>

- [<span data-ttu-id="360a6-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="360a6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

