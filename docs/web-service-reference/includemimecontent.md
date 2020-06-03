---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: Das IncludeMimeContent-Element gibt an, ob der Multipurpose Internet Mail Extensions (MIME) Inhalt eines Elements oder einer Anlage in der Antwort zurückgegeben wird.
ms.openlocfilehash: 6198e4bef2dc59e6e56a8d3cbe463dad13e544e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457193"
---
# <a name="includemimecontent"></a><span data-ttu-id="f3e58-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="f3e58-103">IncludeMimeContent</span></span>

<span data-ttu-id="f3e58-104">Das **IncludeMimeContent** -Element gibt an, ob der Multipurpose Internet Mail Extensions (MIME) Inhalt eines Elements oder einer Anlage in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3e58-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="f3e58-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f3e58-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3e58-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e58-106">Attributes and elements</span></span>

<span data-ttu-id="f3e58-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f3e58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3e58-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3e58-108">Attributes</span></span>

<span data-ttu-id="f3e58-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3e58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3e58-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e58-110">Child elements</span></span>

<span data-ttu-id="f3e58-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3e58-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3e58-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e58-112">Parent elements</span></span>

|<span data-ttu-id="f3e58-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3e58-113">**Element**</span></span>|<span data-ttu-id="f3e58-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3e58-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3e58-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="f3e58-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="f3e58-116">Identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3e58-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="f3e58-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="f3e58-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="f3e58-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="f3e58-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="f3e58-119">Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="f3e58-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="f3e58-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f3e58-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3e58-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="f3e58-121">Text value</span></span>

<span data-ttu-id="f3e58-122">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="f3e58-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="f3e58-123">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f3e58-123">The default value is **false**.</span></span> <span data-ttu-id="f3e58-124">Dies ist ein boolescher Datentyp.</span><span class="sxs-lookup"><span data-stu-id="f3e58-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3e58-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3e58-125">Remarks</span></span>

<span data-ttu-id="f3e58-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="f3e58-126">This element is optional.</span></span>
  
<span data-ttu-id="f3e58-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f3e58-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="f3e58-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3e58-128">Example</span></span>

<span data-ttu-id="f3e58-129">Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie das **IncludeMimeContent** -Element festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f3e58-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
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
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f3e58-130">Das Attribut Attachment ID wird abgeschnitten, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="f3e58-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3e58-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f3e58-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3e58-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3e58-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3e58-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f3e58-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f3e58-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f3e58-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3e58-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f3e58-135">Validation File</span></span>  <br/> |<span data-ttu-id="f3e58-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3e58-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3e58-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f3e58-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3e58-138">False</span><span class="sxs-lookup"><span data-stu-id="f3e58-138">False</span></span>  <br/> |
   

