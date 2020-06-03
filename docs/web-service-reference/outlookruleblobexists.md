---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: Das OutlookRuleBlobExists-Element gibt an, ob ein Microsoft Outlook-Regel-BLOB im Postfach des Benutzers vorhanden ist.
ms.openlocfilehash: 6a5c2a2ec0246d38b22279b86772972ea81922c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529028"
---
# <a name="outlookruleblobexists"></a><span data-ttu-id="05fa5-103">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="05fa5-103">OutlookRuleBlobExists</span></span>

<span data-ttu-id="05fa5-104">Das **OutlookRuleBlobExists** -Element gibt an, ob ein Microsoft Outlook-Regel-BLOB im Postfach des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="05fa5-104">The **OutlookRuleBlobExists** element indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span> 
  
[<span data-ttu-id="05fa5-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="05fa5-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="05fa5-106">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="05fa5-106">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 <span data-ttu-id="05fa5-107">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="05fa5-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05fa5-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05fa5-108">Attributes and elements</span></span>

<span data-ttu-id="05fa5-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05fa5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05fa5-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="05fa5-110">Attributes</span></span>

<span data-ttu-id="05fa5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="05fa5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05fa5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05fa5-112">Child elements</span></span>

<span data-ttu-id="05fa5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="05fa5-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="05fa5-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05fa5-114">Parent elements</span></span>

|<span data-ttu-id="05fa5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="05fa5-115">**Element**</span></span>|<span data-ttu-id="05fa5-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05fa5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05fa5-117">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="05fa5-117">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="05fa5-118">Stellt eine Antwort auf eine [GetInboxRules-Vorgangs](getinboxrules-operation.md) Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="05fa5-118">Represents a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05fa5-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="05fa5-119">Text value</span></span>

<span data-ttu-id="05fa5-120">Der Textwert **true** gibt an, dass ein Outlook-Regel-BLOB vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="05fa5-120">A text value of **true** indicates that an Outlook rule blob exists.</span></span> <span data-ttu-id="05fa5-121">Der Textwert **false** gibt an, dass kein Outlook-Regel-BLOB vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="05fa5-121">A text value of **false** indicates that an Outlook rule blob does not exist.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="05fa5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05fa5-122">Remarks</span></span>

<span data-ttu-id="05fa5-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="05fa5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05fa5-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="05fa5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05fa5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="05fa5-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="05fa5-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05fa5-126">Schema Name</span></span>  <br/> |<span data-ttu-id="05fa5-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="05fa5-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="05fa5-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05fa5-128">Validation File</span></span>  <br/> |<span data-ttu-id="05fa5-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="05fa5-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05fa5-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05fa5-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="05fa5-131">True</span><span class="sxs-lookup"><span data-stu-id="05fa5-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05fa5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05fa5-132">See also</span></span>



- [<span data-ttu-id="05fa5-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="05fa5-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

