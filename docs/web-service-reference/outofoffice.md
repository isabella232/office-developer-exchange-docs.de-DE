---
title: OutOfOffice
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: Das OutOfOffice-Element darstellt, die Antwortnachricht und einer Zeitdauer für die Response-Nachricht senden.
ms.openlocfilehash: 4e1e06ee332c44aeba03e1343c8c3258a2c9631e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830675"
---
# <a name="outofoffice"></a><span data-ttu-id="0dba2-103">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="0dba2-103">OutOfOffice</span></span>

<span data-ttu-id="0dba2-104">Das **OutOfOffice** -Element darstellt, die Antwortnachricht und einer Zeitdauer für die Response-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="0dba2-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

 <span data-ttu-id="0dba2-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="0dba2-105">**OutOfOfficeMailTip**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0dba2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0dba2-106">Attributes and elements</span></span>

<span data-ttu-id="0dba2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0dba2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dba2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0dba2-108">Attributes</span></span>

<span data-ttu-id="0dba2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0dba2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0dba2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0dba2-110">Child elements</span></span>

|<span data-ttu-id="0dba2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dba2-111">**Element**</span></span>|<span data-ttu-id="0dba2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0dba2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dba2-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="0dba2-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="0dba2-114">Enthält eine Nachricht Out of Office (ABWESEND) und die Sprache für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0dba2-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="0dba2-115">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="0dba2-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="0dba2-116">Enthält die Dauer, die der Status ABWESEND aktiviert ist, wenn das Element [OofState](oofstate.md) auf geplante Tasks festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0dba2-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0dba2-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0dba2-117">Parent elements</span></span>

|<span data-ttu-id="0dba2-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dba2-118">**Element**</span></span>|<span data-ttu-id="0dba2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0dba2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dba2-120">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="0dba2-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="0dba2-121">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="0dba2-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0dba2-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="0dba2-122">Text value</span></span>

<span data-ttu-id="0dba2-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="0dba2-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0dba2-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dba2-124">Remarks</span></span>

<span data-ttu-id="0dba2-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0dba2-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dba2-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0dba2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dba2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0dba2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0dba2-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0dba2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0dba2-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0dba2-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="0dba2-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0dba2-130">Validation File</span></span>  <br/> |<span data-ttu-id="0dba2-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0dba2-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0dba2-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0dba2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0dba2-133">False</span><span class="sxs-lookup"><span data-stu-id="0dba2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dba2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dba2-134">See also</span></span>



- [<span data-ttu-id="0dba2-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0dba2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

