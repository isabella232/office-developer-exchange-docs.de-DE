---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: Das MimeContentUTF8-Element enthält den UTF-8-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und die Internationalisierung von e-Mail-Adressen und [RFC6530] unterstützt.
ms.openlocfilehash: a9214bda876c1aadac5b026b3adf38faea8ef17a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530429"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="54c02-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="54c02-103">MimeContentUTF8</span></span>

<span data-ttu-id="54c02-104">Das **MimeContentUTF8** -Element enthält den UTF-8-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und die Internationalisierung von e-Mail-Adressen und [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54c02-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="54c02-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="54c02-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54c02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="54c02-106">Attributes and elements</span></span>

<span data-ttu-id="54c02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="54c02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54c02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="54c02-108">Attributes</span></span>

|<span data-ttu-id="54c02-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="54c02-109">**Attribute**</span></span>|<span data-ttu-id="54c02-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54c02-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54c02-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="54c02-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="54c02-112">Wenn festgelegt, wird der Wert für dieses Attribut vom Server ignoriert.</span><span class="sxs-lookup"><span data-stu-id="54c02-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54c02-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54c02-113">Child elements</span></span>

<span data-ttu-id="54c02-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="54c02-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54c02-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54c02-115">Parent elements</span></span>

<span data-ttu-id="54c02-116">[CalendarItem](calendaritem.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)  |  [Element](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="54c02-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="54c02-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="54c02-117">Text value</span></span>

<span data-ttu-id="54c02-118">Ein Textwert, der einen base64Binary-MIME-Stream darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54c02-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54c02-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54c02-119">Remarks</span></span>

<span data-ttu-id="54c02-120">Der Nachrichteninhalt durchläuft die folgenden drei Codierungs stufen, bevor er im **MimeContentUTF8** -Wert gespeichert wird:</span><span class="sxs-lookup"><span data-stu-id="54c02-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="54c02-121">Nachrichtentext: Dies ist die Textcodierung, beispielsweise ISO-2022-JP für japanische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="54c02-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="54c02-122">MIME-Stream: Dies ist die UTF8-Codierung des Nachrichtentexts für das **MimeContentUTF8** -Element oder die ASCII-Codierung des Nachrichtentexts für das [MimeContent](mimecontent.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="54c02-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="54c02-123">XML-Dokument: Dies ist immer der Base64-codierte ASCII-Datenstrom des MIME-Streams, bei dem Zeichen wie ' \< ', die für XML relevant sind, von XML-Parsern ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="54c02-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="54c02-124">Jede Ebene ist unabhängig von der vorausgehenden Ebene.</span><span class="sxs-lookup"><span data-stu-id="54c02-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="54c02-125">Das **MimeContentUTF8** -Element kann dieselben Daten enthalten, die andere Eigenschaften, die mit einem Element zurückgegeben werden, enthalten.</span><span class="sxs-lookup"><span data-stu-id="54c02-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="54c02-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="54c02-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="54c02-127">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="54c02-127">Version differences</span></span>

<span data-ttu-id="54c02-128">Dieses Element ist in Versionen von Exchange verfügbar, beginnend mit Build 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="54c02-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54c02-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="54c02-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54c02-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="54c02-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54c02-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="54c02-131">Schema Name</span></span>  <br/> |<span data-ttu-id="54c02-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="54c02-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="54c02-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="54c02-133">Validation File</span></span>  <br/> |<span data-ttu-id="54c02-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54c02-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54c02-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="54c02-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="54c02-136">False</span><span class="sxs-lookup"><span data-stu-id="54c02-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54c02-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c02-137">See also</span></span>



- [<span data-ttu-id="54c02-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="54c02-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

