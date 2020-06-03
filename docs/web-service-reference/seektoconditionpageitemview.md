---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: Das SeekToConditionPageItemView-Element gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine FindItem-oder FindConversation-Suche verwendet wird.
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466836"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="c2c25-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="c2c25-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="c2c25-104">Das **SeekToConditionPageItemView** -Element gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine **FindItem** -oder **FindConversation** -Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2c25-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="c2c25-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="c2c25-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2c25-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c2c25-106">Attributes and elements</span></span>

<span data-ttu-id="c2c25-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2c25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2c25-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2c25-108">Attributes</span></span>

|<span data-ttu-id="c2c25-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c2c25-109">**Attribute**</span></span>|<span data-ttu-id="c2c25-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2c25-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2c25-111">Basepoint</span><span class="sxs-lookup"><span data-stu-id="c2c25-111">BasePoint</span></span>  <br/> |<span data-ttu-id="c2c25-112">Der Textwert des **Basepoint** -Attributs ist der Basispunkt, von dem aus die Suche gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c2c25-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="c2c25-113">Der Textwert **Anfang** gibt an, dass die Suche am Anfang der Ergebnismenge beginnt.</span><span class="sxs-lookup"><span data-stu-id="c2c25-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="c2c25-114">Ein Textwert von **End** gibt an, dass die Suche am Ende der Ergebnismenge beginnt.</span><span class="sxs-lookup"><span data-stu-id="c2c25-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="c2c25-115">MaxEntriesReturned</span><span class="sxs-lookup"><span data-stu-id="c2c25-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="c2c25-116">Der Textwert des **MaxEntriesReturned** -Attributs ist die maximale Anzahl von Elementen, die in einer Ergebnismenge zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c2c25-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c2c25-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2c25-117">Child elements</span></span>

[<span data-ttu-id="c2c25-118">Condition (restrictiontype)</span><span class="sxs-lookup"><span data-stu-id="c2c25-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="c2c25-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2c25-119">Parent elements</span></span>

<span data-ttu-id="c2c25-120">[FindConversation](findconversation.md)  |  [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="c2c25-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2c25-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2c25-121">Remarks</span></span>

<span data-ttu-id="c2c25-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2c25-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2c25-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c2c25-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2c25-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c2c25-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2c25-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2c25-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2c25-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c2c25-126">Schema name</span></span>  <br/> |<span data-ttu-id="c2c25-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c2c25-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2c25-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c2c25-128">Validation file</span></span>  <br/> |<span data-ttu-id="c2c25-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c2c25-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2c25-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c2c25-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c2c25-131">False</span><span class="sxs-lookup"><span data-stu-id="c2c25-131">false</span></span>  <br/> |
   

