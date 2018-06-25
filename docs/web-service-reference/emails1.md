---
title: Emails1
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cc02bd86-c618-446a-92f0-749423cbc4ee
description: Das Emails1-Element gibt ein Array von Werten EmailAddressAttributedValue und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: f1a1223244c91731b1a5a1beb9daed6d680d3bc4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758180"
---
# <a name="emails1"></a><span data-ttu-id="f0ed6-103">Emails1</span><span class="sxs-lookup"><span data-stu-id="f0ed6-103">Emails1</span></span>

<span data-ttu-id="f0ed6-104">Das **Emails1** -Element gibt ein Array von Werten **EmailAddressAttributedValue** und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-104">The **Emails1** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails1>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails1>
```

 <span data-ttu-id="f0ed6-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f0ed6-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0ed6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f0ed6-106">Attributes and elements</span></span>

<span data-ttu-id="f0ed6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0ed6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0ed6-108">Attributes</span></span>

<span data-ttu-id="f0ed6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0ed6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0ed6-110">Child elements</span></span>

|<span data-ttu-id="f0ed6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0ed6-111">**Element**</span></span>|<span data-ttu-id="f0ed6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0ed6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ed6-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f0ed6-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="f0ed6-114">Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0ed6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0ed6-115">Parent elements</span></span>

|<span data-ttu-id="f0ed6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0ed6-116">**Element**</span></span>|<span data-ttu-id="f0ed6-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0ed6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ed6-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="f0ed6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f0ed6-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ed6-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0ed6-120">Remarks</span></span>

<span data-ttu-id="f0ed6-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f0ed6-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f0ed6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0ed6-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f0ed6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0ed6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0ed6-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0ed6-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f0ed6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f0ed6-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="f0ed6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f0ed6-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f0ed6-127">Validation File</span></span>  <br/> |<span data-ttu-id="f0ed6-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0ed6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0ed6-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f0ed6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f0ed6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0ed6-130">See also</span></span>



- [<span data-ttu-id="f0ed6-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0ed6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

