---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: Das ItemShape-Element identifiziert eine Reihe von Eigenschaften, die in einer GetItem-Operation, einer FindItem-Operation oder einer SyncFolderItems-Vorgangs Antwort zurückgegeben werden sollen.
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458124"
---
# <a name="itemshape"></a><span data-ttu-id="e6377-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="e6377-103">ItemShape</span></span>

<span data-ttu-id="e6377-104">Das **ItemShape** -Element identifiziert eine Reihe von Eigenschaften, die in einer [GetItem-Operation](getitem-operation.md), einer [FindItem-Operation](finditem-operation.md)oder einer SyncFolderItems- [Vorgangs](syncfolderitems-operation.md) Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6377-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 <span data-ttu-id="e6377-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="e6377-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6377-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6377-106">Attributes and elements</span></span>

<span data-ttu-id="e6377-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6377-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6377-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6377-108">Attributes</span></span>

<span data-ttu-id="e6377-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6377-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6377-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6377-110">Child elements</span></span>

|<span data-ttu-id="e6377-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6377-111">**Element**</span></span>|<span data-ttu-id="e6377-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6377-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6377-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="e6377-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="e6377-114">Gibt die grundlegende Konfiguration von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6377-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="e6377-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="e6377-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="e6377-116">Gibt an, ob der Multipurpose Internet Mail Extensions (MIME) Inhalt eines Elements in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6377-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="e6377-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="e6377-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="e6377-118">Gibt an, wie der Textkörper in der Antwort formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="e6377-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="e6377-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="e6377-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="e6377-120">Gibt an, ob der Element-HTML-Text in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="e6377-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="e6377-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="e6377-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="e6377-122">Gibt an, ob die HTML-Inhaltsfilterung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6377-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="e6377-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e6377-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="e6377-124">Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6377-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6377-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6377-125">Parent elements</span></span>

|<span data-ttu-id="e6377-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6377-126">**Element**</span></span>|<span data-ttu-id="e6377-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6377-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6377-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="e6377-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="e6377-129">Definiert eine Anforderung zum Abrufen von Elementen aus einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e6377-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="e6377-130">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="e6377-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="e6377-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="e6377-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e6377-132">Definiert eine Anforderung zum Suchen aller Elemente, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e6377-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="e6377-133">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="e6377-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="e6377-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e6377-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="e6377-135">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="e6377-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="e6377-136">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="e6377-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e6377-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="e6377-137">Text value</span></span>

<span data-ttu-id="e6377-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6377-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6377-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6377-139">Remarks</span></span>

<span data-ttu-id="e6377-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e6377-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6377-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e6377-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6377-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6377-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6377-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6377-143">Schema Name</span></span>  <br/> |<span data-ttu-id="e6377-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e6377-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6377-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6377-145">Validation File</span></span>  <br/> |<span data-ttu-id="e6377-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e6377-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6377-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e6377-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6377-148">False</span><span class="sxs-lookup"><span data-stu-id="e6377-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6377-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6377-149">See also</span></span>



[<span data-ttu-id="e6377-150">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6377-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="e6377-151">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6377-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="e6377-152">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6377-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="e6377-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e6377-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

