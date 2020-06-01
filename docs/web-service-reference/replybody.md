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
description: Das ReplyBody-Element enthält eine Abwesenheit (Out of Office, OOF) Nachricht und die für die Nachricht verwendete Sprache.
ms.openlocfilehash: 496d336d1f87d9ea493ba7da362eef5a416fd899
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465303"
---
# <a name="replybody"></a><span data-ttu-id="c8d29-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="c8d29-103">ReplyBody</span></span>

<span data-ttu-id="c8d29-104">Das **ReplyBody** -Element enthält eine Abwesenheit (Out of Office, OOF) Nachricht und die für die Nachricht verwendete Sprache.</span><span class="sxs-lookup"><span data-stu-id="c8d29-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="c8d29-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="c8d29-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8d29-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c8d29-106">Attributes and elements</span></span>

<span data-ttu-id="c8d29-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c8d29-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8d29-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c8d29-108">Attributes</span></span>

|<span data-ttu-id="c8d29-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c8d29-109">**Attribute**</span></span>|<span data-ttu-id="c8d29-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8d29-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8d29-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="c8d29-111">xml:lang</span></span>  <br/> |<span data-ttu-id="c8d29-112">Gibt die Sprache an, die im **ReplyBody** -Inhalt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8d29-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="c8d29-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="c8d29-113">This attribute is optional.</span></span> <span data-ttu-id="c8d29-114">Die möglichen Werte dieses Attributs werden durch IETF RFC 3066 definiert.</span><span class="sxs-lookup"><span data-stu-id="c8d29-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8d29-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8d29-115">Child elements</span></span>

|<span data-ttu-id="c8d29-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8d29-116">**Element**</span></span>|<span data-ttu-id="c8d29-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8d29-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8d29-118">Message (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="c8d29-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="c8d29-119">Enthält die Abwesenheitsantwort (Abwesenheit von Office).</span><span class="sxs-lookup"><span data-stu-id="c8d29-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8d29-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8d29-120">Parent elements</span></span>

|<span data-ttu-id="c8d29-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8d29-121">**Element**</span></span>|<span data-ttu-id="c8d29-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8d29-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8d29-123">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="c8d29-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="c8d29-124">Definiert die Abwesenheitsantwort Nachricht und einen Zeitraum für das Senden der Antwortnachricht für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="c8d29-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8d29-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="c8d29-125">Text value</span></span>

<span data-ttu-id="c8d29-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8d29-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8d29-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d29-127">Remarks</span></span>

<span data-ttu-id="c8d29-128">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8d29-128">This element is required.</span></span>
  
<span data-ttu-id="c8d29-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c8d29-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8d29-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c8d29-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8d29-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8d29-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8d29-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c8d29-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c8d29-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c8d29-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8d29-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c8d29-134">Validation File</span></span>  <br/> |<span data-ttu-id="c8d29-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8d29-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8d29-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c8d29-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8d29-137">False</span><span class="sxs-lookup"><span data-stu-id="c8d29-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8d29-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d29-138">See also</span></span>



- [<span data-ttu-id="c8d29-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c8d29-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

