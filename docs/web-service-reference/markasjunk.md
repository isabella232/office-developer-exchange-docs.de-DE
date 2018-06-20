---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: Das MarkAsJunk-Element gibt die Anforderung zum Verschieben eines Elements in den Junk-e-Mailordner und den Absender zur Liste blockierter Absender hinzufügen.
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830350"
---
# <a name="markasjunk"></a><span data-ttu-id="4984c-103">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4984c-103">MarkAsJunk</span></span>

<span data-ttu-id="4984c-104">Das **MarkAsJunk** -Element gibt die Anforderung zum Verschieben eines Elements in den Junk-e-Mailordner und den Absender zur Liste blockierter Absender hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4984c-104">The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list.</span></span> 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 <span data-ttu-id="4984c-105">**MarkAsJunkType**</span><span class="sxs-lookup"><span data-stu-id="4984c-105">**MarkAsJunkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4984c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4984c-106">Attributes and elements</span></span>

<span data-ttu-id="4984c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4984c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4984c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4984c-108">Attributes</span></span>

|<span data-ttu-id="4984c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4984c-109">**Attribute**</span></span>|<span data-ttu-id="4984c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4984c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4984c-111">IsJunk</span><span class="sxs-lookup"><span data-stu-id="4984c-111">IsJunk</span></span>  <br/> |<span data-ttu-id="4984c-112">Der Textwert **true** für das **IsJunk** -Attribut gibt an, dass der e-Mail-Absender zur Liste blockierter Absender hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4984c-112">A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list.</span></span> <span data-ttu-id="4984c-113">Der Wert **false** gibt an, dass der e-Mail-Absender aus der Liste blockierter Absender entfernt wird, wenn der e-Mail-Absender bereits in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="4984c-113">A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.</span></span>  <br/> |
|<span data-ttu-id="4984c-114">MoveItem</span><span class="sxs-lookup"><span data-stu-id="4984c-114">MoveItem</span></span>  <br/> |<span data-ttu-id="4984c-115">Der Textwert **true** für das **MoveItem** -Attribut gibt an, dass das Element in der standardmäßigen Junk-e-Mail-Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="4984c-115">A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder.</span></span> <span data-ttu-id="4984c-116">Der Wert **false** gibt an, dass das Element nicht in den Junk-e-Mail-Standardordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="4984c-116">A value of **false** indicates that the item is not moved to the default junk mail folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4984c-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4984c-117">Child elements</span></span>

[<span data-ttu-id="4984c-118">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="4984c-118">ItemIds</span></span>](itemids.md)
  
### <a name="parent-elements"></a><span data-ttu-id="4984c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4984c-119">Parent elements</span></span>

<span data-ttu-id="4984c-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="4984c-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4984c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4984c-121">Remarks</span></span>

<span data-ttu-id="4984c-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4984c-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4984c-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4984c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4984c-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4984c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4984c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4984c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4984c-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4984c-126">Schema name</span></span>  <br/> |<span data-ttu-id="4984c-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4984c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4984c-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4984c-128">Validation file</span></span>  <br/> |<span data-ttu-id="4984c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4984c-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4984c-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4984c-130">Can be empty</span></span>  <br/> ||
   

