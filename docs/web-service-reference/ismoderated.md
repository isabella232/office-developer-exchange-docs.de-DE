---
title: Ismoderiert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: Das ismoded-Element gibt an, ob das Postfach des Empfängers moderiert wird.
ms.openlocfilehash: 930d5a7e09712f35d22850a93462d051a34785a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435485"
---
# <a name="ismoderated"></a><span data-ttu-id="ec5e5-103">Ismoderiert</span><span class="sxs-lookup"><span data-stu-id="ec5e5-103">IsModerated</span></span>

<span data-ttu-id="ec5e5-104">Das **ismoded** -Element gibt an, ob das Postfach des Empfängers moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="ec5e5-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ec5e5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec5e5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec5e5-106">Attributes and elements</span></span>

<span data-ttu-id="ec5e5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec5e5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec5e5-108">Attributes</span></span>

<span data-ttu-id="ec5e5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec5e5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec5e5-110">Child elements</span></span>

<span data-ttu-id="ec5e5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec5e5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec5e5-112">Parent elements</span></span>

|<span data-ttu-id="ec5e5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec5e5-113">**Element**</span></span>|<span data-ttu-id="ec5e5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec5e5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec5e5-115">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="ec5e5-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="ec5e5-116">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec5e5-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec5e5-117">Text value</span></span>

<span data-ttu-id="ec5e5-118">Der Textwert für dieses Element ist **true** , wenn das Postfach des Empfängers moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="ec5e5-119">Der Wert ist **false** , wenn das Postfach des Empfängers nicht moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ec5e5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec5e5-120">Remarks</span></span>

<span data-ttu-id="ec5e5-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ec5e5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec5e5-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ec5e5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec5e5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec5e5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec5e5-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec5e5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ec5e5-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ec5e5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec5e5-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec5e5-126">Validation File</span></span>  <br/> |<span data-ttu-id="ec5e5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec5e5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec5e5-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec5e5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec5e5-129">False</span><span class="sxs-lookup"><span data-stu-id="ec5e5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec5e5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec5e5-130">See also</span></span>



- [<span data-ttu-id="ec5e5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec5e5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

