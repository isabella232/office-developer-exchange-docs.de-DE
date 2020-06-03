---
title: Text
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a71a75f0-0b77-4cb9-8f9d-319de72fc1fd
description: Das Bodys-Element gibt ein Array von BodyContentAttributedValue-Elementen an.
ms.openlocfilehash: d7087cf213d3c659a55458e021f4b8f0400efb1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461513"
---
# <a name="bodies"></a><span data-ttu-id="86874-103">Text</span><span class="sxs-lookup"><span data-stu-id="86874-103">Bodies</span></span>

<span data-ttu-id="86874-104">Das **Bodys** -Element gibt ein Array von **BodyContentAttributedValue** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="86874-104">The **Bodies** element specifies an array of **BodyContentAttributedValue** elements.</span></span> 
  
```XML
<Bodies>
    <BodyContentAttributedValue></BodyContentAttributedValue>
<Bodies>
```

 <span data-ttu-id="86874-105">**ArrayOfBodyContentAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="86874-105">**ArrayOfBodyContentAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86874-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86874-106">Attributes and elements</span></span>

<span data-ttu-id="86874-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86874-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86874-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86874-108">Attributes</span></span>

<span data-ttu-id="86874-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="86874-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86874-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86874-110">Child elements</span></span>

|<span data-ttu-id="86874-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="86874-111">**Element**</span></span>|<span data-ttu-id="86874-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86874-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86874-113">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="86874-113">BodyContentAttributedValue</span></span>](bodycontentattributedvalue.md) <br/> |<span data-ttu-id="86874-114">Gibt den Textkörper Inhalt eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="86874-114">Specifies the body content of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86874-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86874-115">Parent elements</span></span>

|<span data-ttu-id="86874-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="86874-116">**Element**</span></span>|<span data-ttu-id="86874-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86874-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86874-118">Persona</span><span class="sxs-lookup"><span data-stu-id="86874-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="86874-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="86874-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86874-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86874-120">Remarks</span></span>

<span data-ttu-id="86874-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="86874-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="86874-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86874-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86874-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="86874-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86874-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="86874-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86874-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86874-125">Schema Name</span></span>  <br/> |<span data-ttu-id="86874-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="86874-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="86874-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86874-127">Validation File</span></span>  <br/> |<span data-ttu-id="86874-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="86874-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="86874-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="86874-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="86874-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86874-130">See also</span></span>



- [<span data-ttu-id="86874-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="86874-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

