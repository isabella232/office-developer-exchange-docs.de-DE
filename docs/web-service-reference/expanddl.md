---
title: Der ExpandDL
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
description: Das Element der ExpandDL definiert eine Anforderung an eine Verteilerliste erweitern.
ms.openlocfilehash: ef93ed4684427a74a4fd2c38b4020ecb743fbaaf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758311"
---
# <a name="expanddl"></a><span data-ttu-id="823ec-103">Der ExpandDL</span><span class="sxs-lookup"><span data-stu-id="823ec-103">ExpandDL</span></span>

<span data-ttu-id="823ec-104">Das Element **der ExpandDL** definiert eine Anforderung an eine Verteilerliste erweitern.</span><span class="sxs-lookup"><span data-stu-id="823ec-104">The **ExpandDL** element defines a request to expand a distribution list.</span></span> 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 <span data-ttu-id="823ec-105">**ExpandDLType**</span><span class="sxs-lookup"><span data-stu-id="823ec-105">**ExpandDLType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="823ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="823ec-106">Attributes and elements</span></span>

<span data-ttu-id="823ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="823ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="823ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="823ec-108">Attributes</span></span>

<span data-ttu-id="823ec-109">Keine</span><span class="sxs-lookup"><span data-stu-id="823ec-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="823ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="823ec-110">Child elements</span></span>

|<span data-ttu-id="823ec-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="823ec-111">**Element**</span></span>|<span data-ttu-id="823ec-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="823ec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="823ec-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="823ec-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="823ec-114">Identifiziert eine vollständig aufgelöster E-mail-Adresse oder eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="823ec-114">Identifies a fully resolved e-mail address or a distribution list.</span></span> <span data-ttu-id="823ec-115">Dieses Postfach stellt die Verteilerliste zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="823ec-115">This mailbox represents the distribution list to expand.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="823ec-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="823ec-116">Parent elements</span></span>

<span data-ttu-id="823ec-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="823ec-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="823ec-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="823ec-118">Remarks</span></span>

<span data-ttu-id="823ec-119">Eine Erweiterung der Verteilerliste wird nur für eine Verteilerliste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="823ec-119">A distribution list expansion will only be performed for a single distribution list.</span></span> <span data-ttu-id="823ec-120">Eine Erweiterung der Verteilerliste ist nicht rekursiv.</span><span class="sxs-lookup"><span data-stu-id="823ec-120">A distribution list expansion is not recursive.</span></span>
  
<span data-ttu-id="823ec-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="823ec-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="823ec-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="823ec-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="823ec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="823ec-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="823ec-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="823ec-124">Schema Name</span></span>  <br/> |<span data-ttu-id="823ec-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="823ec-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="823ec-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="823ec-126">Validation File</span></span>  <br/> |<span data-ttu-id="823ec-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="823ec-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="823ec-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="823ec-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="823ec-129">False</span><span class="sxs-lookup"><span data-stu-id="823ec-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="823ec-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="823ec-130">See also</span></span>



[<span data-ttu-id="823ec-131">Der ExpandDL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="823ec-131">ExpandDL operation</span></span>](expanddl-operation.md)

