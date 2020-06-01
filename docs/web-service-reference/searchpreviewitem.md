---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: Das SearchPreviewItem-Element gibt die Elementvorschau für eine Ermittlungs Suche an.
ms.openlocfilehash: ab48353b0ffaf4bc3b9409f1a620d145bffc7a13
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466934"
---
# <a name="searchpreviewitem"></a><span data-ttu-id="21874-103">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="21874-103">SearchPreviewItem</span></span>

<span data-ttu-id="21874-104">Das **SearchPreviewItem** -Element gibt die Elementvorschau für eine Ermittlungs Suche an.</span><span class="sxs-lookup"><span data-stu-id="21874-104">The **SearchPreviewItem** element specifies the item preview for a discovery search.</span></span> 
  
```XML
<SearchPreviewItem>
   <Id/>
   <Mailbox/>
   <ParentId/>
   <ItemClass/>
   <UniqueHash/>
   <SortValue/>
   <OwaLink/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <CreatedTime/>
   <ReceivedTime/>
   <SentTime/>
   <Subject/>
   <Size/>
   <Preview/>
   <Importance/>
   <Read/>
   <HasAttachment/>
   <ExtendedProperties/>
</SearchPreviewItem>
```

 <span data-ttu-id="21874-105">**SearchPreviewItemType**</span><span class="sxs-lookup"><span data-stu-id="21874-105">**SearchPreviewItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21874-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21874-106">Attributes and elements</span></span>

<span data-ttu-id="21874-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21874-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21874-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="21874-108">Attributes</span></span>

<span data-ttu-id="21874-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="21874-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21874-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21874-110">Child elements</span></span>

<span data-ttu-id="21874-111">[ID (itemidtype)](id-itemidtype.md)  |  [Postfach (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md)  |  [Übergeordnete-Nr](parentid.md)  |  [ItemClass](itemclass.md)  |  [UniqueHash](uniquehash.md)  |  [Sortvalue](sortvalue.md)  |  [OwaLink](owalink.md)  |  [Absender (Zeichenfolge)](sender-string.md)  |  [Torecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md)  |  [CcRecipients](ccrecipients.md)  |  [BccRecipients](bccrecipients.md)  |  [Erstellt am](createdtime.md)  |  Empfangs Zeitteile [ReceivedTime](receivedtime.md)  |  [Sentzeit](senttime.md)  |  [Betreff](subject.md)  |  [Größe (lang)](size-long.md)  |  [Vorschau anzeigen](preview-ex15websvcsotherref.md)  |  [Wichtigkeit](importance.md)  |  [Lesen Sie](read.md)  |  [Hatanlage](hasattachment.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span><span class="sxs-lookup"><span data-stu-id="21874-111">[ID (ItemIdType)](id-itemidtype.md) | [Mailbox (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md) | [Sender (string)](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md) | [SentTime](senttime.md) | [Subject](subject.md) | [Size (long)](size-long.md) | [Preview](preview-ex15websvcsotherref.md) | [Importance](importance.md) | [Read](read.md) | [HasAttachment](hasattachment.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21874-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21874-112">Parent elements</span></span>

[<span data-ttu-id="21874-113">Elemente (ArrayOfSearchPreviewItemsType)</span><span class="sxs-lookup"><span data-stu-id="21874-113">Items (ArrayOfSearchPreviewItemsType)</span></span>](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a><span data-ttu-id="21874-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21874-114">Remarks</span></span>

<span data-ttu-id="21874-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="21874-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="21874-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="21874-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21874-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="21874-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21874-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="21874-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21874-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21874-119">Schema name</span></span>  <br/> |<span data-ttu-id="21874-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="21874-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="21874-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21874-121">Validation file</span></span>  <br/> |<span data-ttu-id="21874-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21874-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21874-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="21874-123">Can be empty</span></span>  <br/> ||
   

