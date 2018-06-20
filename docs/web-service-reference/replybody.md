---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: Das ReplyBody-Element enthält eine Nachricht Out of Office (ABWESEND) und die Sprache für die Nachricht verwendet.
ms.openlocfilehash: 8400dda1ee810781e129fcc44fd3cd5d6c15cbbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831116"
---
# <a name="replybody"></a><span data-ttu-id="f91bc-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="f91bc-103">ReplyBody</span></span>

<span data-ttu-id="f91bc-104">Das **ReplyBody** -Element enthält eine Nachricht Out of Office (ABWESEND) und die Sprache für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f91bc-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="f91bc-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="f91bc-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f91bc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f91bc-106">Attributes and elements</span></span>

<span data-ttu-id="f91bc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f91bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f91bc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f91bc-108">Attributes</span></span>

|<span data-ttu-id="f91bc-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f91bc-109">**Attribute**</span></span>|<span data-ttu-id="f91bc-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f91bc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f91bc-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="f91bc-111">xml:lang</span></span>  <br/> |<span data-ttu-id="f91bc-112">Gibt die Sprache, die in den **ReplyBody** Inhalt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f91bc-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="f91bc-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f91bc-113">This attribute is optional.</span></span> <span data-ttu-id="f91bc-114">Die möglichen Werte dieses Attributs werden durch IETF RFC 3066 definiert.</span><span class="sxs-lookup"><span data-stu-id="f91bc-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f91bc-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f91bc-115">Child elements</span></span>

|<span data-ttu-id="f91bc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f91bc-116">**Element**</span></span>|<span data-ttu-id="f91bc-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f91bc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f91bc-118">Nachricht (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f91bc-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="f91bc-119">Enthält die Abwesenheitsnotiz Besprechungsthema-Antwort.</span><span class="sxs-lookup"><span data-stu-id="f91bc-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f91bc-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f91bc-120">Parent elements</span></span>

|<span data-ttu-id="f91bc-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f91bc-121">**Element**</span></span>|<span data-ttu-id="f91bc-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f91bc-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f91bc-123">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="f91bc-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="f91bc-124">Definiert die Antwort Abwesenheitsnachricht und eine Dauer für das Senden der Antwortnachricht für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="f91bc-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f91bc-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f91bc-125">Text value</span></span>

<span data-ttu-id="f91bc-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="f91bc-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f91bc-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f91bc-127">Remarks</span></span>

<span data-ttu-id="f91bc-128">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f91bc-128">This element is required.</span></span>
  
<span data-ttu-id="f91bc-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f91bc-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f91bc-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f91bc-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f91bc-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f91bc-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f91bc-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f91bc-132">Schema Name</span></span>  <br/> |<span data-ttu-id="f91bc-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f91bc-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f91bc-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f91bc-134">Validation File</span></span>  <br/> |<span data-ttu-id="f91bc-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f91bc-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f91bc-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f91bc-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="f91bc-137">False</span><span class="sxs-lookup"><span data-stu-id="f91bc-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f91bc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f91bc-138">See also</span></span>



- [<span data-ttu-id="f91bc-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f91bc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

