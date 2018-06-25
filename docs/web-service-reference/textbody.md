---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: Das TextBody-Element gibt den Textkörper.
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839176"
---
# <a name="textbody"></a><span data-ttu-id="9bf22-103">TextBody</span><span class="sxs-lookup"><span data-stu-id="9bf22-103">TextBody</span></span>

<span data-ttu-id="9bf22-104">Das **TextBody** -Element gibt den Textkörper.</span><span class="sxs-lookup"><span data-stu-id="9bf22-104">The **TextBody** element specifies the text body.</span></span> 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 <span data-ttu-id="9bf22-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="9bf22-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bf22-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf22-106">Attributes and elements</span></span>

<span data-ttu-id="9bf22-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9bf22-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bf22-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9bf22-108">Attributes</span></span>

|<span data-ttu-id="9bf22-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9bf22-109">**Attribute**</span></span>|<span data-ttu-id="9bf22-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9bf22-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bf22-111">BodyTypeType</span><span class="sxs-lookup"><span data-stu-id="9bf22-111">BodyTypeType</span></span>  <br/> |<span data-ttu-id="9bf22-112">Gibt den Typ des Hauptteils an.</span><span class="sxs-lookup"><span data-stu-id="9bf22-112">Indicates the body type.</span></span> <span data-ttu-id="9bf22-113">Der Wert der **Text** für das **BodyTypeType** -Attribut gibt an, dass der Text in nur-Text-Format ist.</span><span class="sxs-lookup"><span data-stu-id="9bf22-113">The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="9bf22-114">Der Wert von **HTML** für das **BodyTypeType** -Attribut gibt an, dass der Textkörper in HTML-Formular ist.</span><span class="sxs-lookup"><span data-stu-id="9bf22-114">The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="9bf22-115">Das Attribut **BodyTypeType** ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9bf22-115">The **BodyTypeType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9bf22-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="9bf22-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="9bf22-117">Gibt an, dass der Inhalt des Body abgeschnitten worden sein.</span><span class="sxs-lookup"><span data-stu-id="9bf22-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="9bf22-118">Der Textwert **false** für das **IsTruncated** -Attribut gibt an, dass der Inhalt des Body nicht abgeschnitten worden sein.</span><span class="sxs-lookup"><span data-stu-id="9bf22-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="9bf22-119">Normalisierte Textkörper werden abgeschnitten, wenn die Länge des Hauptteils Text länger als der Wert im [MaximumBodySize](maximumbodysize.md) -Element festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9bf22-119">The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9bf22-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf22-120">Child elements</span></span>

<span data-ttu-id="9bf22-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="9bf22-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9bf22-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf22-122">Parent elements</span></span>

<span data-ttu-id="9bf22-123">[Element](item.md) | [Kontakt](contact.md) | [Nachricht](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="9bf22-123">[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9bf22-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="9bf22-124">Text value</span></span>

<span data-ttu-id="9bf22-125">Der Textwert des **TextBody** -Elements ist der Textkörper des Elements.</span><span class="sxs-lookup"><span data-stu-id="9bf22-125">The text value of the **TextBody** element is the text body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9bf22-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9bf22-126">Remarks</span></span>

<span data-ttu-id="9bf22-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9bf22-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9bf22-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9bf22-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bf22-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9bf22-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bf22-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bf22-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9bf22-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9bf22-131">Schema name</span></span>  <br/> |<span data-ttu-id="9bf22-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9bf22-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="9bf22-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9bf22-133">Validation file</span></span>  <br/> |<span data-ttu-id="9bf22-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9bf22-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9bf22-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9bf22-135">Can be empty</span></span>  <br/> ||
   

