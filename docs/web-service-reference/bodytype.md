---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: Das BodyType-Element identifiziert, wie der Textkörper in der Antwort formatiert ist.
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757479"
---
# <a name="bodytype"></a><span data-ttu-id="8d08e-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="8d08e-103">BodyType</span></span>

<span data-ttu-id="8d08e-104">Das **BodyType** -Element identifiziert, wie der Textkörper in der Antwort formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d08e-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="8d08e-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="8d08e-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8d08e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d08e-106">Attributes and elements</span></span>

<span data-ttu-id="8d08e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d08e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d08e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d08e-108">Attributes</span></span>

<span data-ttu-id="8d08e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d08e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d08e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d08e-110">Child elements</span></span>

<span data-ttu-id="8d08e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d08e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d08e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d08e-112">Parent elements</span></span>

|<span data-ttu-id="8d08e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d08e-113">**Element**</span></span>|<span data-ttu-id="8d08e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d08e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d08e-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="8d08e-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="8d08e-116">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8d08e-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="8d08e-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="8d08e-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="8d08e-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="8d08e-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="8d08e-119">Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückzugebenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8d08e-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="8d08e-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="8d08e-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d08e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8d08e-121">Text value</span></span>

<span data-ttu-id="8d08e-122">Die folgende Tabelle enthält die möglichen Werte für das Element **"BodyType"** .</span><span class="sxs-lookup"><span data-stu-id="8d08e-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="8d08e-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8d08e-123">**Value**</span></span>|<span data-ttu-id="8d08e-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d08e-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d08e-125">Am besten</span><span class="sxs-lookup"><span data-stu-id="8d08e-125">Best</span></span>  <br/> |<span data-ttu-id="8d08e-126">Die Antwort wird den inhaltlich verfügbaren Inhalt des Textkörpers zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8d08e-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="8d08e-127">Dies ist nützlich, wenn nicht bekannt ist, ob der Inhalt Text "oder" HTML ist.</span><span class="sxs-lookup"><span data-stu-id="8d08e-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="8d08e-128">Der zurückgegebene Text ist Text wird, wenn der gespeicherte Text nur-Text.</span><span class="sxs-lookup"><span data-stu-id="8d08e-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="8d08e-129">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper in HTML oder RTF-Format ist.</span><span class="sxs-lookup"><span data-stu-id="8d08e-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="8d08e-130">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8d08e-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="8d08e-131">HTML</span><span class="sxs-lookup"><span data-stu-id="8d08e-131">HTML</span></span>  <br/> |<span data-ttu-id="8d08e-132">Die Antwort wird ein Textkörper im HTML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="8d08e-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="8d08e-133">Text</span><span class="sxs-lookup"><span data-stu-id="8d08e-133">Text</span></span>  <br/> |<span data-ttu-id="8d08e-134">Die Antwort wird ein Textkörper als nur-Text zurück.</span><span class="sxs-lookup"><span data-stu-id="8d08e-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d08e-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d08e-135">Remarks</span></span>

<span data-ttu-id="8d08e-136">Sie können den Typ des Mobilgeräts **BodyType** -Attribut des [Body](body.md) -Elements in der Antwort zurückgegebenen Textkörper identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8d08e-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="8d08e-137">Das Attribut **BodyType** erkennt den Text als HTML oder Text.</span><span class="sxs-lookup"><span data-stu-id="8d08e-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="8d08e-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8d08e-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="8d08e-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8d08e-139">Example</span></span>

<span data-ttu-id="8d08e-140">Im folgenden Beispiel wird eine Anforderung zeigt, wo ein **BodyType** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d08e-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8d08e-141">Das Id-Attribut wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d08e-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d08e-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d08e-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d08e-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d08e-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d08e-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d08e-144">Schema Name</span></span>  <br/> |<span data-ttu-id="8d08e-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d08e-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d08e-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d08e-146">Validation File</span></span>  <br/> |<span data-ttu-id="8d08e-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d08e-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d08e-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8d08e-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d08e-149">False</span><span class="sxs-lookup"><span data-stu-id="8d08e-149">False</span></span>  <br/> |
   

