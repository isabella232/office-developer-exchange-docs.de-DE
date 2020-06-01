---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: Das GetImItems-Anforderungselement definiert eine Anforderung zum Abrufen von Informationen über die angegebenen Chatgruppen und Kontaktpersonen für Chatnachrichten.
ms.openlocfilehash: e3973cbbf800ffe91472b9c733c4d4a927b91c9f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456451"
---
# <a name="getimitems"></a><span data-ttu-id="447f4-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="447f4-103">GetImItems</span></span>

<span data-ttu-id="447f4-104">Das **GetImItems** -Anforderungselement definiert eine Anforderung zum Abrufen von Informationen über die angegebenen Chatgruppen und Kontaktpersonen für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="447f4-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="447f4-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="447f4-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="447f4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="447f4-106">Attributes and elements</span></span>

<span data-ttu-id="447f4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="447f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="447f4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="447f4-108">Attributes</span></span>

<span data-ttu-id="447f4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="447f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="447f4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="447f4-110">Child elements</span></span>

<span data-ttu-id="447f4-111">[ContactIds](contactids.md) Die  |  [GroupIds](groupids.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="447f4-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="447f4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="447f4-112">Parent elements</span></span>

<span data-ttu-id="447f4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="447f4-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="447f4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="447f4-114">Remarks</span></span>

<span data-ttu-id="447f4-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="447f4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="447f4-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="447f4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="447f4-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="447f4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="447f4-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="447f4-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="447f4-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="447f4-119">Schema name</span></span>  <br/> |<span data-ttu-id="447f4-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="447f4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="447f4-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="447f4-121">Validation file</span></span>  <br/> |<span data-ttu-id="447f4-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="447f4-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="447f4-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="447f4-123">Can be empty</span></span>  <br/> ||
   

