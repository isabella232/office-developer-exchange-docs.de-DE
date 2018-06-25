---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: Das IsQuickContact-Element gibt einen Boolean-Wert, der angibt, ob der zugrunde liegende Kontakt ein schnelles Kontakt ist.
ms.openlocfilehash: 979dbd3c0358eacd443eed79b258f7dd6bb9bc7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830092"
---
# <a name="isquickcontact"></a><span data-ttu-id="50da0-103">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="50da0-103">IsQuickContact</span></span>

<span data-ttu-id="50da0-104">Das **IsQuickContact** -Element gibt einen Boolean-Wert, der angibt, ob der zugrunde liegende Kontakt ein schnelles Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="50da0-104">The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact.</span></span> 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 <span data-ttu-id="50da0-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="50da0-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50da0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50da0-106">Attributes and elements</span></span>

<span data-ttu-id="50da0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50da0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50da0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50da0-108">Attributes</span></span>

<span data-ttu-id="50da0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50da0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50da0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50da0-110">Child elements</span></span>

<span data-ttu-id="50da0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="50da0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50da0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50da0-112">Parent elements</span></span>

|<span data-ttu-id="50da0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="50da0-113">**Element**</span></span>|<span data-ttu-id="50da0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50da0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50da0-115">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="50da0-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="50da0-116">Gibt eine Instanz in ein Array von Attributen für eine **Rolle** -Element an.</span><span class="sxs-lookup"><span data-stu-id="50da0-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50da0-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="50da0-117">Text value</span></span>

<span data-ttu-id="50da0-118">Der Textwert **true** für das **IsQuickContact** -Element gibt an, dass der Kontakt ein schnelles Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="50da0-118">A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact.</span></span> <span data-ttu-id="50da0-119">Der Wert **false** gibt an, dass der Kontakt keinen schnellen Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="50da0-119">A value of **false** indicates that the contact is not a quick contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50da0-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50da0-120">Remarks</span></span>

<span data-ttu-id="50da0-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50da0-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50da0-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="50da0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50da0-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="50da0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50da0-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="50da0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50da0-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50da0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="50da0-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="50da0-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="50da0-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50da0-127">Validation File</span></span>  <br/> |<span data-ttu-id="50da0-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50da0-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="50da0-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="50da0-129">Can Be Empty</span></span>  <br/> |<span data-ttu-id="50da0-130">false</span><span class="sxs-lookup"><span data-stu-id="50da0-130">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50da0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50da0-131">See also</span></span>



- [<span data-ttu-id="50da0-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="50da0-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

