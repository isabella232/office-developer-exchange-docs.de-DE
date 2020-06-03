---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: Das MimeContent-Element enthält den ASCII-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und [RFC2045] unterstützt.
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530436"
---
# <a name="mimecontent"></a><span data-ttu-id="ad327-103">MimeContent</span><span class="sxs-lookup"><span data-stu-id="ad327-103">MimeContent</span></span>

<span data-ttu-id="ad327-104">Das **MimeContent** -Element enthält den ASCII-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad327-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="ad327-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="ad327-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad327-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad327-106">Attributes and elements</span></span>

<span data-ttu-id="ad327-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad327-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad327-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad327-108">Attributes</span></span>

|<span data-ttu-id="ad327-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad327-109">**Attribute**</span></span>|<span data-ttu-id="ad327-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad327-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad327-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="ad327-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="ad327-112">Wenn festgelegt, wird der Wert für dieses Attribut vom Server ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ad327-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad327-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad327-113">Child elements</span></span>

<span data-ttu-id="ad327-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad327-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad327-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad327-115">Parent elements</span></span>

<span data-ttu-id="ad327-116">[CalendarItem](calendaritem.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)  |  [Element](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="ad327-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ad327-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ad327-117">Text value</span></span>

<span data-ttu-id="ad327-118">Ein Textwert, der einen base64Binary-MIME-Stream darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad327-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad327-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad327-119">Remarks</span></span>

<span data-ttu-id="ad327-120">Der Nachrichteninhalt durchläuft die folgenden drei Codierungs stufen, bevor er im **MimeContent** -Wert gespeichert wird:</span><span class="sxs-lookup"><span data-stu-id="ad327-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="ad327-121">Nachrichtentext: Dies ist die Textcodierung, beispielsweise ISO-2022-JP für japanische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ad327-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="ad327-122">MIME-Stream: Dies ist die ASCII-Codierung des Nachrichtentexts für das **MimeContent** -Element oder die UTF8-Codierung des Nachrichtentexts für das [MimeContentUTF8](mimecontentutf8.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ad327-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="ad327-123">XML-Dokument: Dies ist immer der Base64-codierte ASCII-Datenstrom des MIME-Streams, bei dem Zeichen wie ' \< ', die für XML relevant sind, von XML-Parsern ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad327-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="ad327-124">Jede Ebene ist unabhängig von der vorausgehenden Ebene.</span><span class="sxs-lookup"><span data-stu-id="ad327-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="ad327-125">Das **MimeContent** -Element kann dieselben Daten enthalten, die andere Eigenschaften, die mit einem Element zurückgegeben werden, enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad327-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="ad327-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ad327-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad327-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ad327-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad327-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad327-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad327-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad327-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ad327-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ad327-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad327-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad327-131">Validation File</span></span>  <br/> |<span data-ttu-id="ad327-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad327-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad327-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ad327-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad327-134">False</span><span class="sxs-lookup"><span data-stu-id="ad327-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad327-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad327-135">See also</span></span>



- [<span data-ttu-id="ad327-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad327-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

