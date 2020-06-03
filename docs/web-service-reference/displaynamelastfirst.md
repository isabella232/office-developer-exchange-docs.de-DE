---
title: DisplayNameLastFirst
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d392e138-a514-4bce-81b1-1f484e353d1c
description: Das DisplayNameLastFirst-Element gibt den Anzeigenamen der zugeordneten Persona in Format, Nachname und Vorname an.
ms.openlocfilehash: d569a87ce77a4f1840ed4f865e671399726ede78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463160"
---
# <a name="displaynamelastfirst"></a><span data-ttu-id="7fd00-103">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="7fd00-103">DisplayNameLastFirst</span></span>

<span data-ttu-id="7fd00-104">Das **DisplayNameLastFirst** -Element gibt den Anzeigenamen der zugeordneten Persona im Format "Nachname", "Vorname" an.</span><span class="sxs-lookup"><span data-stu-id="7fd00-104">The **DisplayNameLastFirst** element specifies the display name of the associated persona in the format, "Last Name", "First Name".</span></span> 
  
```XML
<DisplayNameLastFirst></DisplayNameLastFirst>
```

 <span data-ttu-id="7fd00-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7fd00-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fd00-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd00-106">Attributes and elements</span></span>

<span data-ttu-id="7fd00-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fd00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fd00-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fd00-108">Attributes</span></span>

<span data-ttu-id="7fd00-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fd00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fd00-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd00-110">Child elements</span></span>

<span data-ttu-id="7fd00-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fd00-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7fd00-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd00-112">Parent elements</span></span>

|<span data-ttu-id="7fd00-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fd00-113">**Element**</span></span>|<span data-ttu-id="7fd00-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fd00-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd00-115">Persona</span><span class="sxs-lookup"><span data-stu-id="7fd00-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="7fd00-116">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fd00-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fd00-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="7fd00-117">Text value</span></span>

<span data-ttu-id="7fd00-118">Der Textwert des **DisplayNameLastFirst** -Elements ist ein String-Wert, der den Anzeigenamen mit dem Namen First angibt.</span><span class="sxs-lookup"><span data-stu-id="7fd00-118">The text value of the **DisplayNameLastFirst** element is a string value that specifies the display name, with the surname first.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7fd00-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd00-119">Remarks</span></span>

<span data-ttu-id="7fd00-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fd00-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7fd00-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7fd00-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fd00-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7fd00-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fd00-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fd00-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fd00-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fd00-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7fd00-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="7fd00-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="7fd00-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fd00-126">Validation File</span></span>  <br/> |<span data-ttu-id="7fd00-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7fd00-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fd00-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7fd00-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7fd00-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fd00-129">See also</span></span>

- [<span data-ttu-id="7fd00-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fd00-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

