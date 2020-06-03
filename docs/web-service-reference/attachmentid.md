---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: Das Attachments-Element identifiziert ein Element oder eine Dateianlage. Dieses Element wird in CreateAttachment-Antworten verwendet.
ms.openlocfilehash: b5dc9299b615f0fc01b8afcbaabf0ec7996e53d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459111"
---
# <a name="attachmentid"></a><span data-ttu-id="ce1c4-104">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="ce1c4-104">AttachmentId</span></span>

<span data-ttu-id="ce1c4-105">Das **Attachments** -Element identifiziert ein Element oder eine Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-105">The **AttachmentId** element identifies an item or file attachment.</span></span> <span data-ttu-id="ce1c4-106">Dieses Element wird in CreateAttachment-Antworten verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-106">This element is used in CreateAttachment responses.</span></span> 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="ce1c4-107">**AttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-107">**AttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce1c4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ce1c4-108">Attributes and elements</span></span>

<span data-ttu-id="ce1c4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce1c4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce1c4-110">Attributes</span></span>

|<span data-ttu-id="ce1c4-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-111">**Attribute**</span></span>|<span data-ttu-id="ce1c4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce1c4-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-113">**Id**</span></span> <br/> |<span data-ttu-id="ce1c4-114">Gibt den eindeutigen Bezeichner der Anlage an.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-114">Identifies the unique identifier of the attachment.</span></span>  <br/> |
|<span data-ttu-id="ce1c4-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="ce1c4-116">Gibt den eindeutigen Bezeichner des Stammspeicher Elements an, an das die Anlage angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-116">Identifies the unique identifier of the root store item to which the attachment is attached.</span></span>  <br/> |
|<span data-ttu-id="ce1c4-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="ce1c4-118">Gibt den Änderungsschlüssel des Stammspeicher Elements an, an das die Anlage angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-118">Identifies the change key of the root store item to which the attachment is attached.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce1c4-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce1c4-119">Child elements</span></span>

<span data-ttu-id="ce1c4-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce1c4-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce1c4-121">Parent elements</span></span>

|<span data-ttu-id="ce1c4-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-122">**Element**</span></span>|<span data-ttu-id="ce1c4-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce1c4-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce1c4-124">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="ce1c4-124">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="ce1c4-125">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-125">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="ce1c4-126">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="ce1c4-126">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="ce1c4-127">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-127">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce1c4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce1c4-128">Remarks</span></span>

<span data-ttu-id="ce1c4-129">Es ist wichtig zu beachten, dass beim Erstellen einer Anlage der Änderungsschlüssel des Stammelements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-129">It is important to note that when an attachment is created, the change key of the root item is altered.</span></span>
  
<span data-ttu-id="ce1c4-130">Das [Attachment-Element (GetAttachment und DeleteAttachment-)](attachmentid-getattachment-and-deleteattachment.md) wird in DeleteAttachment--und GetAttachment-Anforderungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-130">The [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) element is used in DeleteAttachment and GetAttachment requests.</span></span> 
  
<span data-ttu-id="ce1c4-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ce1c4-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce1c4-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ce1c4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce1c4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce1c4-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce1c4-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ce1c4-134">Schema name</span></span>  <br/> |<span data-ttu-id="ce1c4-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ce1c4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce1c4-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ce1c4-136">Validation file</span></span>  <br/> |<span data-ttu-id="ce1c4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce1c4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce1c4-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ce1c4-138">Can be empty</span></span>  <br/> |<span data-ttu-id="ce1c4-139">False</span><span class="sxs-lookup"><span data-stu-id="ce1c4-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce1c4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce1c4-140">See also</span></span>

- [<span data-ttu-id="ce1c4-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ce1c4-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

