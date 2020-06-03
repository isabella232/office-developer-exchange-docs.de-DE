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
description: Das BodyType-Element gibt an, wie der Textkörper in der Antwort formatiert wird.
ms.openlocfilehash: 448d20ac54b09a2f4f6a273a1099519371ac7f5b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465947"
---
# <a name="bodytype"></a><span data-ttu-id="0ab17-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="0ab17-103">BodyType</span></span>

<span data-ttu-id="0ab17-104">Das **BodyType** -Element gibt an, wie der Textkörper in der Antwort formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ab17-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="0ab17-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="0ab17-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0ab17-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0ab17-106">Attributes and elements</span></span>

<span data-ttu-id="0ab17-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0ab17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ab17-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0ab17-108">Attributes</span></span>

<span data-ttu-id="0ab17-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ab17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ab17-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ab17-110">Child elements</span></span>

<span data-ttu-id="0ab17-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ab17-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0ab17-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ab17-112">Parent elements</span></span>

|<span data-ttu-id="0ab17-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ab17-113">**Element**</span></span>|<span data-ttu-id="0ab17-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ab17-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ab17-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="0ab17-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="0ab17-116">Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0ab17-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="0ab17-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="0ab17-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="0ab17-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="0ab17-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="0ab17-119">Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ab17-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="0ab17-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="0ab17-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ab17-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="0ab17-121">Text value</span></span>

<span data-ttu-id="0ab17-122">In der folgenden Tabelle sind die möglichen Werte für das **BodyType** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ab17-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="0ab17-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0ab17-123">**Value**</span></span>|<span data-ttu-id="0ab17-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ab17-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ab17-125">Optimal</span><span class="sxs-lookup"><span data-stu-id="0ab17-125">Best</span></span>  <br/> |<span data-ttu-id="0ab17-126">Die Antwort gibt den reichsten verfügbaren Inhalt des Textkörpers zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab17-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="0ab17-127">Dies ist hilfreich, wenn unbekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.</span><span class="sxs-lookup"><span data-stu-id="0ab17-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="0ab17-128">Der zurückgegebene Text ist Text, wenn der gespeicherte Text nur-Text ist.</span><span class="sxs-lookup"><span data-stu-id="0ab17-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="0ab17-129">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Text im HTML-oder RTF-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="0ab17-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="0ab17-130">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="0ab17-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="0ab17-131">HTML</span><span class="sxs-lookup"><span data-stu-id="0ab17-131">HTML</span></span>  <br/> |<span data-ttu-id="0ab17-132">Die Antwort gibt einen Element Text als HTML zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab17-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="0ab17-133">Text</span><span class="sxs-lookup"><span data-stu-id="0ab17-133">Text</span></span>  <br/> |<span data-ttu-id="0ab17-134">Die Antwort gibt einen Element Text als nur-Text zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab17-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ab17-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ab17-135">Remarks</span></span>

<span data-ttu-id="0ab17-136">Sie können den Typ des in der Antwort zurückgegebenen Textkörpers identifizieren, indem Sie das **BodyType** -Attribut des [Body](body.md) -Elements überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0ab17-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="0ab17-137">Das **BodyType** -Attribut identifiziert den Text entweder als HTML oder als Text.</span><span class="sxs-lookup"><span data-stu-id="0ab17-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="0ab17-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0ab17-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="0ab17-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ab17-139">Example</span></span>

<span data-ttu-id="0ab17-140">Im folgenden Beispiel einer Anforderung wird gezeigt, wo ein **BodyType** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ab17-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="0ab17-141">Das ID-Attribut wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="0ab17-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ab17-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0ab17-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ab17-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ab17-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ab17-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0ab17-144">Schema Name</span></span>  <br/> |<span data-ttu-id="0ab17-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0ab17-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="0ab17-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0ab17-146">Validation File</span></span>  <br/> |<span data-ttu-id="0ab17-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0ab17-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ab17-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0ab17-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ab17-149">False</span><span class="sxs-lookup"><span data-stu-id="0ab17-149">False</span></span>  <br/> |
   

