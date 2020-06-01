---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: Das MarkAsJunk-Element gibt die Anforderung an, ein Element in den Ordner Junk-e-Mail zu migrieren und den Absender der Liste blockierter Absender hinzuzufügen.
ms.openlocfilehash: 99adc423864f3096772394ef290df20e158e457d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467081"
---
# <a name="markasjunk"></a><span data-ttu-id="28687-103">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="28687-103">MarkAsJunk</span></span>

<span data-ttu-id="28687-104">Das **MarkAsJunk** -Element gibt die Anforderung an, ein Element in den Ordner Junk-e-Mail zu migrieren und den Absender der Liste blockierter Absender hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="28687-104">The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list.</span></span> 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 <span data-ttu-id="28687-105">**MarkAsJunkType**</span><span class="sxs-lookup"><span data-stu-id="28687-105">**MarkAsJunkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28687-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28687-106">Attributes and elements</span></span>

<span data-ttu-id="28687-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28687-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28687-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28687-108">Attributes</span></span>

|<span data-ttu-id="28687-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="28687-109">**Attribute**</span></span>|<span data-ttu-id="28687-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28687-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28687-111">Isjunk</span><span class="sxs-lookup"><span data-stu-id="28687-111">IsJunk</span></span>  <br/> |<span data-ttu-id="28687-112">Der Textwert **true** für das **isjunk** -Attribut gibt an, dass der e-Mail-Absender der Liste blockierter Absender hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="28687-112">A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list.</span></span> <span data-ttu-id="28687-113">Der Wert **false** gibt an, dass der e-Mail-Absender aus der Liste blockierter Absender entfernt wird, wenn sich der e-Mail-Absender bereits in der Liste befindet.</span><span class="sxs-lookup"><span data-stu-id="28687-113">A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.</span></span>  <br/> |
|<span data-ttu-id="28687-114">MoveItem</span><span class="sxs-lookup"><span data-stu-id="28687-114">MoveItem</span></span>  <br/> |<span data-ttu-id="28687-115">Der Textwert **true** für das **MoveItem** -Attribut gibt an, dass das Element in den standardmäßigen Junk-e-Mail-Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="28687-115">A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder.</span></span> <span data-ttu-id="28687-116">Der Wert **false** gibt an, dass das Element nicht in den standardmäßigen Junk-e-Mail-Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="28687-116">A value of **false** indicates that the item is not moved to the default junk mail folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28687-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28687-117">Child elements</span></span>

[<span data-ttu-id="28687-118">ItemIds</span><span class="sxs-lookup"><span data-stu-id="28687-118">ItemIds</span></span>](itemids.md)
  
### <a name="parent-elements"></a><span data-ttu-id="28687-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28687-119">Parent elements</span></span>

<span data-ttu-id="28687-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="28687-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28687-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28687-121">Remarks</span></span>

<span data-ttu-id="28687-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28687-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="28687-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="28687-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28687-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28687-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28687-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="28687-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28687-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28687-126">Schema name</span></span>  <br/> |<span data-ttu-id="28687-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="28687-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28687-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28687-128">Validation file</span></span>  <br/> |<span data-ttu-id="28687-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="28687-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28687-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="28687-130">Can be empty</span></span>  <br/> ||
   

