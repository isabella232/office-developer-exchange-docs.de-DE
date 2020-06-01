---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: Das TextBody-Element gibt den Textkörper an.
ms.openlocfilehash: c0002785fb990a251267218f7a5f232e521db41a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459483"
---
# <a name="textbody"></a><span data-ttu-id="111ab-103">TextBody</span><span class="sxs-lookup"><span data-stu-id="111ab-103">TextBody</span></span>

<span data-ttu-id="111ab-104">Das **TextBody** -Element gibt den Textkörper an.</span><span class="sxs-lookup"><span data-stu-id="111ab-104">The **TextBody** element specifies the text body.</span></span> 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 <span data-ttu-id="111ab-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="111ab-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="111ab-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="111ab-106">Attributes and elements</span></span>

<span data-ttu-id="111ab-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="111ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="111ab-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="111ab-108">Attributes</span></span>

|<span data-ttu-id="111ab-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="111ab-109">**Attribute**</span></span>|<span data-ttu-id="111ab-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="111ab-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="111ab-111">BodyTypeType</span><span class="sxs-lookup"><span data-stu-id="111ab-111">BodyTypeType</span></span>  <br/> |<span data-ttu-id="111ab-112">Gibt den Typ des Texts an.</span><span class="sxs-lookup"><span data-stu-id="111ab-112">Indicates the body type.</span></span> <span data-ttu-id="111ab-113">Der Wert des **Texts** für das **BodyTypeType** -Attribut gibt an, dass sich der Text im nur-Text-Format befindet.</span><span class="sxs-lookup"><span data-stu-id="111ab-113">The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="111ab-114">Der Wert von **HTML** für das **BodyTypeType** -Attribut gibt an, dass sich der Text im HTML-Format befindet.</span><span class="sxs-lookup"><span data-stu-id="111ab-114">The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="111ab-115">Das **BodyTypeType** -Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="111ab-115">The **BodyTypeType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="111ab-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="111ab-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="111ab-117">Gibt an, dass der Textkörper Inhalt abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="111ab-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="111ab-118">Der Textwert **false** für das Attribut **IsTruncated** gibt an, dass der Inhalt des Texts nicht abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="111ab-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="111ab-119">Der normalisierte Text wird abgeschnitten, wenn die Textkörper Länge länger ist als der im [MaximumBodySize](maximumbodysize.md) -Element festgelegte Wert.</span><span class="sxs-lookup"><span data-stu-id="111ab-119">The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="111ab-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="111ab-120">Child elements</span></span>

<span data-ttu-id="111ab-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="111ab-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="111ab-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="111ab-122">Parent elements</span></span>

<span data-ttu-id="111ab-123">[Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [Verteilerliste](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="111ab-123">[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="111ab-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="111ab-124">Text value</span></span>

<span data-ttu-id="111ab-125">Der TextText-Wert des **TextBody** -Elements ist der Textkörper des Elements.</span><span class="sxs-lookup"><span data-stu-id="111ab-125">The text value of the **TextBody** element is the text body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="111ab-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="111ab-126">Remarks</span></span>

<span data-ttu-id="111ab-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="111ab-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="111ab-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="111ab-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="111ab-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="111ab-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="111ab-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="111ab-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="111ab-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="111ab-131">Schema name</span></span>  <br/> |<span data-ttu-id="111ab-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="111ab-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="111ab-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="111ab-133">Validation file</span></span>  <br/> |<span data-ttu-id="111ab-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="111ab-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="111ab-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="111ab-135">Can be empty</span></span>  <br/> ||
   

