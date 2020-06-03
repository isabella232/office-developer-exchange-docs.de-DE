---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: Das UpdatedItemIds-Element gibt die Bezeichner der aktualisierten Reminder-Elemente an.
ms.openlocfilehash: 4a87bf50f90e80c0c887ee3a66b9f201ea1c8440
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465036"
---
# <a name="updateditemids"></a><span data-ttu-id="543b4-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="543b4-103">UpdatedItemIds</span></span>

<span data-ttu-id="543b4-104">Das **UpdatedItemIds** -Element gibt die Bezeichner der aktualisierten Reminder-Elemente an.</span><span class="sxs-lookup"><span data-stu-id="543b4-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="543b4-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="543b4-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="543b4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="543b4-106">Attributes and elements</span></span>

<span data-ttu-id="543b4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="543b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="543b4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="543b4-108">Attributes</span></span>

<span data-ttu-id="543b4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="543b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="543b4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="543b4-110">Child elements</span></span>

[<span data-ttu-id="543b4-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="543b4-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="543b4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="543b4-112">Parent elements</span></span>

[<span data-ttu-id="543b4-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="543b4-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="543b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="543b4-114">Remarks</span></span>

<span data-ttu-id="543b4-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="543b4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="543b4-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="543b4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="543b4-117">Wenn der [PerformReminderAction](performreminderaction-operation.md) -Vorgang nicht erfolgreich abgeschlossen wurde oder keine Änderungen auf dem Server vorgenommen wurden, wird das **UpdatedItemIds** -Element als leerer Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="543b4-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="543b4-118">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="543b4-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="543b4-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="543b4-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="543b4-120">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="543b4-120">Schema Name</span></span>  <br/> |<span data-ttu-id="543b4-121">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="543b4-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="543b4-122">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="543b4-122">Validation File</span></span>  <br/> |<span data-ttu-id="543b4-123">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="543b4-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="543b4-124">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="543b4-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="543b4-125">True</span><span class="sxs-lookup"><span data-stu-id="543b4-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="543b4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="543b4-126">See also</span></span>



[<span data-ttu-id="543b4-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="543b4-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="543b4-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="543b4-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

