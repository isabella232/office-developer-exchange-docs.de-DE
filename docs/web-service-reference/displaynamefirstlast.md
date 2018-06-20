---
title: DisplayNameFirstLast
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 013c17c9-cb37-4028-9fe6-c3f47441d0f7
description: Das DisplayNameFirstLast-Element gibt den Anzeigenamen der zugeordneten Rolle im Format, Vorname, Nachname.
ms.openlocfilehash: 7a8c269c7e1b03448d176a630fbcae979926bdf4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758056"
---
# <a name="displaynamefirstlast"></a><span data-ttu-id="a9aa1-103">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="a9aa1-103">DisplayNameFirstLast</span></span>

<span data-ttu-id="a9aa1-104">Das **DisplayNameFirstLast** -Element gibt den Anzeigenamen der zugeordneten Rolle im Format "First Name", "Nachname".</span><span class="sxs-lookup"><span data-stu-id="a9aa1-104">The **DisplayNameFirstLast** element specifies the display name of the associated persona in the format, "First Name", "Last Name".</span></span> 
  
```XML
<DisplayNameFirstLast>
```

 <span data-ttu-id="a9aa1-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a9aa1-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9aa1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9aa1-106">Attributes and elements</span></span>

<span data-ttu-id="a9aa1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9aa1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9aa1-108">Attributes</span></span>

<span data-ttu-id="a9aa1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9aa1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9aa1-110">Child elements</span></span>

<span data-ttu-id="a9aa1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9aa1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9aa1-112">Parent elements</span></span>

|<span data-ttu-id="a9aa1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9aa1-113">**Element**</span></span>|<span data-ttu-id="a9aa1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9aa1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9aa1-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="a9aa1-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="a9aa1-116">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9aa1-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="a9aa1-117">Text value</span></span>

<span data-ttu-id="a9aa1-118">Der Textwert der **DisplayNameFirstLast** -Element ist ein String-Wert, der den Anzeigenamen, mit dem angegebenen Namen zuerst enthält.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-118">The text value of the **DisplayNameFirstLast** element is a string value containing the display name, with the given name first.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a9aa1-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9aa1-119">Remarks</span></span>

<span data-ttu-id="a9aa1-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a9aa1-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a9aa1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9aa1-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a9aa1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9aa1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9aa1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9aa1-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9aa1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a9aa1-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="a9aa1-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="a9aa1-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9aa1-126">Validation File</span></span>  <br/> |<span data-ttu-id="a9aa1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9aa1-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9aa1-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a9aa1-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a9aa1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9aa1-129">See also</span></span>

- [<span data-ttu-id="a9aa1-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a9aa1-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

