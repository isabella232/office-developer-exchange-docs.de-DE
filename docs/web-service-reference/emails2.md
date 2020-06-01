---
title: Emails2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6ad95936-f61b-431a-9d86-df160b5d4b2d
description: Das Emails2-Element enthält ein Array von EmailAddressAttributedValue-Werten und die Bezeichner der Quell Zuweisungen für die zugeordnete Persona.
ms.openlocfilehash: b9445dfdc556ade1ad96d6e56c35ec1e56627e8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463412"
---
# <a name="emails2"></a><span data-ttu-id="29ce4-103">Emails2</span><span class="sxs-lookup"><span data-stu-id="29ce4-103">Emails2</span></span>

<span data-ttu-id="29ce4-104">Das **Emails2** -Element enthält ein Array von **EmailAddressAttributedValue** -Werten und die Bezeichner der Quell Zuweisungen für die zugeordnete Persona.</span><span class="sxs-lookup"><span data-stu-id="29ce4-104">The **Emails2** element contains an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails2>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails2>
```

 <span data-ttu-id="29ce4-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="29ce4-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29ce4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="29ce4-106">Attributes and elements</span></span>

<span data-ttu-id="29ce4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="29ce4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29ce4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="29ce4-108">Attributes</span></span>

<span data-ttu-id="29ce4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="29ce4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29ce4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29ce4-110">Child elements</span></span>

|<span data-ttu-id="29ce4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="29ce4-111">**Element**</span></span>|<span data-ttu-id="29ce4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29ce4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ce4-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="29ce4-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="29ce4-114">Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="29ce4-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="29ce4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29ce4-115">Parent elements</span></span>

|<span data-ttu-id="29ce4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="29ce4-116">**Element**</span></span>|<span data-ttu-id="29ce4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29ce4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ce4-118">Persona</span><span class="sxs-lookup"><span data-stu-id="29ce4-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="29ce4-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="29ce4-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ce4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29ce4-120">Remarks</span></span>

<span data-ttu-id="29ce4-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="29ce4-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="29ce4-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="29ce4-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29ce4-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="29ce4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29ce4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="29ce4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29ce4-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="29ce4-125">Schema Name</span></span>  <br/> |<span data-ttu-id="29ce4-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="29ce4-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="29ce4-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="29ce4-127">Validation File</span></span>  <br/> |<span data-ttu-id="29ce4-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="29ce4-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="29ce4-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="29ce4-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="29ce4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ce4-130">See also</span></span>



- [<span data-ttu-id="29ce4-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="29ce4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

