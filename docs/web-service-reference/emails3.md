---
title: Emails3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dc589-4530-4a35-b2a6-0c83cac23637
description: Das Emails3-Element gibt ein Array von Werten EmailAddressAttributedValue und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 1d174000d59883446bb7f61af90278d197ef5ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758184"
---
# <a name="emails3"></a><span data-ttu-id="1c45e-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="1c45e-103">Emails3</span></span>

<span data-ttu-id="1c45e-104">Das **Emails3** -Element gibt ein Array von Werten **EmailAddressAttributedValue** und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="1c45e-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="1c45e-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="1c45e-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c45e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c45e-106">Attributes and elements</span></span>

<span data-ttu-id="1c45e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c45e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c45e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c45e-108">Attributes</span></span>

<span data-ttu-id="1c45e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c45e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c45e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c45e-110">Child elements</span></span>

|<span data-ttu-id="1c45e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c45e-111">**Element**</span></span>|<span data-ttu-id="1c45e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c45e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c45e-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1c45e-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="1c45e-114">Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1c45e-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1c45e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c45e-115">Parent elements</span></span>

|<span data-ttu-id="1c45e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c45e-116">**Element**</span></span>|<span data-ttu-id="1c45e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c45e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c45e-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="1c45e-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="1c45e-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1c45e-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c45e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c45e-120">Remarks</span></span>

<span data-ttu-id="1c45e-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1c45e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c45e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1c45e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c45e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c45e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c45e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c45e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c45e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c45e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1c45e-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1c45e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1c45e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c45e-127">Validation File</span></span>  <br/> |<span data-ttu-id="1c45e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1c45e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c45e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1c45e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1c45e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c45e-130">See also</span></span>



- [<span data-ttu-id="1c45e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1c45e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

