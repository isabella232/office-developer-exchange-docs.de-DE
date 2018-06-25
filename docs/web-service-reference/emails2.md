---
title: Emails2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6ad95936-f61b-431a-9d86-df160b5d4b2d
description: Das Emails2-Element enthält ein Array von Werten EmailAddressAttributedValue und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 1767d6bfaee335717e33e0345c605025a073335c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758179"
---
# <a name="emails2"></a><span data-ttu-id="fd10f-103">Emails2</span><span class="sxs-lookup"><span data-stu-id="fd10f-103">Emails2</span></span>

<span data-ttu-id="fd10f-104">Das **Emails2** -Element enthält ein Array von Werten **EmailAddressAttributedValue** und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="fd10f-104">The **Emails2** element contains an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails2>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails2>
```

 <span data-ttu-id="fd10f-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="fd10f-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd10f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fd10f-106">Attributes and elements</span></span>

<span data-ttu-id="fd10f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fd10f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd10f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd10f-108">Attributes</span></span>

<span data-ttu-id="fd10f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd10f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd10f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd10f-110">Child elements</span></span>

|<span data-ttu-id="fd10f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd10f-111">**Element**</span></span>|<span data-ttu-id="fd10f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd10f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd10f-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="fd10f-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="fd10f-114">Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fd10f-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fd10f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd10f-115">Parent elements</span></span>

|<span data-ttu-id="fd10f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd10f-116">**Element**</span></span>|<span data-ttu-id="fd10f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd10f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd10f-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="fd10f-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="fd10f-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd10f-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd10f-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd10f-120">Remarks</span></span>

<span data-ttu-id="fd10f-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fd10f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fd10f-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fd10f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd10f-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fd10f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd10f-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd10f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd10f-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fd10f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fd10f-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="fd10f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fd10f-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd10f-127">Validation File</span></span>  <br/> |<span data-ttu-id="fd10f-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd10f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd10f-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fd10f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fd10f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd10f-130">See also</span></span>



- [<span data-ttu-id="fd10f-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd10f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

