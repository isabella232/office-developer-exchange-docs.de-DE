---
title: ExpandDL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: affe84a5-ad98-4aba-83f4-8732938b763d
description: Das ExpandDL-Element definiert eine Anforderung zum Erweitern einer Verteilerliste.
ms.openlocfilehash: 52b1ea1b51ce185c7a266e3002a4484e4b813bc0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456934"
---
# <a name="expanddl"></a><span data-ttu-id="33e2e-103">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="33e2e-103">ExpandDL</span></span>

<span data-ttu-id="33e2e-104">Das **ExpandDL** -Element definiert eine Anforderung zum Erweitern einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="33e2e-104">The **ExpandDL** element defines a request to expand a distribution list.</span></span> 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 <span data-ttu-id="33e2e-105">**ExpandDLType**</span><span class="sxs-lookup"><span data-stu-id="33e2e-105">**ExpandDLType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33e2e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="33e2e-106">Attributes and elements</span></span>

<span data-ttu-id="33e2e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="33e2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33e2e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="33e2e-108">Attributes</span></span>

<span data-ttu-id="33e2e-109">Keine</span><span class="sxs-lookup"><span data-stu-id="33e2e-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33e2e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33e2e-110">Child elements</span></span>

|<span data-ttu-id="33e2e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="33e2e-111">**Element**</span></span>|<span data-ttu-id="33e2e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33e2e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33e2e-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="33e2e-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="33e2e-114">Identifiziert eine vollständig aufgelöste e-Mail-Adresse oder eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="33e2e-114">Identifies a fully resolved e-mail address or a distribution list.</span></span> <span data-ttu-id="33e2e-115">Dieses Postfach stellt die zu erweiternde Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="33e2e-115">This mailbox represents the distribution list to expand.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33e2e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33e2e-116">Parent elements</span></span>

<span data-ttu-id="33e2e-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="33e2e-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33e2e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e2e-118">Remarks</span></span>

<span data-ttu-id="33e2e-119">Eine Verteilerlistenerweiterung wird nur für eine einzelne Verteilerliste ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33e2e-119">A distribution list expansion will only be performed for a single distribution list.</span></span> <span data-ttu-id="33e2e-120">Eine Verteilerlistenerweiterung ist nicht rekursiv.</span><span class="sxs-lookup"><span data-stu-id="33e2e-120">A distribution list expansion is not recursive.</span></span>
  
<span data-ttu-id="33e2e-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="33e2e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33e2e-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="33e2e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33e2e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="33e2e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="33e2e-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="33e2e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="33e2e-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="33e2e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="33e2e-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="33e2e-126">Validation File</span></span>  <br/> |<span data-ttu-id="33e2e-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="33e2e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="33e2e-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="33e2e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="33e2e-129">False</span><span class="sxs-lookup"><span data-stu-id="33e2e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33e2e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e2e-130">See also</span></span>



[<span data-ttu-id="33e2e-131">ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="33e2e-131">ExpandDL operation</span></span>](expanddl-operation.md)

