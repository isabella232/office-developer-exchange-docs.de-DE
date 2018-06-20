---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: Das RemoveOutlookRuleBlob-Element gibt an, ob das Microsoft Outlook-Regel Blob entfernt.
ms.openlocfilehash: 45336e296c39161704ce6e0d51fba1d2c61797b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831102"
---
# <a name="removeoutlookruleblob"></a><span data-ttu-id="c40b7-103">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="c40b7-103">RemoveOutlookRuleBlob</span></span>

<span data-ttu-id="c40b7-104">Das **RemoveOutlookRuleBlob** -Element gibt an, ob das Microsoft Outlook-Regel Blob entfernt.</span><span class="sxs-lookup"><span data-stu-id="c40b7-104">The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob.</span></span> 
  
[<span data-ttu-id="c40b7-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c40b7-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="c40b7-106">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="c40b7-106">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 <span data-ttu-id="c40b7-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c40b7-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c40b7-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c40b7-108">Attributes and elements</span></span>

<span data-ttu-id="c40b7-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c40b7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c40b7-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c40b7-110">Attributes</span></span>

<span data-ttu-id="c40b7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c40b7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c40b7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c40b7-112">Child elements</span></span>

<span data-ttu-id="c40b7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c40b7-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c40b7-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c40b7-114">Parent elements</span></span>

|<span data-ttu-id="c40b7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c40b7-115">**Element**</span></span>|<span data-ttu-id="c40b7-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c40b7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c40b7-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c40b7-117">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="c40b7-118">Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="c40b7-118">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c40b7-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c40b7-119">Text value</span></span>

<span data-ttu-id="c40b7-120">Der Textwert **true** gibt an, dass der Outlook-Regel Blob entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c40b7-120">A text value of **true** indicates that the Outlook rule blob should be removed.</span></span> <span data-ttu-id="c40b7-121">Der Textwert **false** gibt an, dass der Outlook-Regel Blob nicht entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c40b7-121">A text value of **false** indicates that the Outlook rule blob should not be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c40b7-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c40b7-122">Remarks</span></span>

<span data-ttu-id="c40b7-123">Legen Sie dieses Element auf **true fest,** um ein Posteingang Regel Update zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c40b7-123">Set this element to **true** to allow for an Inbox rule update.</span></span> 
  
<span data-ttu-id="c40b7-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c40b7-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c40b7-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c40b7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c40b7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c40b7-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c40b7-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c40b7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c40b7-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c40b7-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c40b7-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c40b7-129">Validation File</span></span>  <br/> |<span data-ttu-id="c40b7-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c40b7-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c40b7-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c40b7-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="c40b7-132">True</span><span class="sxs-lookup"><span data-stu-id="c40b7-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c40b7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c40b7-133">See also</span></span>



[<span data-ttu-id="c40b7-134">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c40b7-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="c40b7-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c40b7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

