---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: Das RetentionPolicyTag-Element gibt die Aufbewahrungsrichtlinie für ein Postfachelement an.
ms.openlocfilehash: 3ece841e14e6cf11ab15e4a4d8b83a778ae32e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465177"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="c4a22-103">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="c4a22-103">RetentionPolicyTag</span></span>

<span data-ttu-id="c4a22-104">Das **RetentionPolicyTag** -Element gibt die Aufbewahrungsrichtlinie für ein Postfachelement an.</span><span class="sxs-lookup"><span data-stu-id="c4a22-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
```XML
<RetentionPolicyTag>
   <DisplayName/>
   <RetentionId/>
   <RetentionPeriod/>
   <Type/>
   <RetentionAction/>
   <Description/>
   <IsVisible/>
   <OptedInto/>
   <IsArchive/>
</RetentionPolicyTag>
```

 <span data-ttu-id="c4a22-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="c4a22-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4a22-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4a22-106">Attributes and elements</span></span>

<span data-ttu-id="c4a22-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4a22-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4a22-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4a22-108">Attributes</span></span>

<span data-ttu-id="c4a22-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4a22-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4a22-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4a22-110">Child elements</span></span>

<span data-ttu-id="c4a22-111">[DisplayName (Zeichenfolge)](displayname-string.md)  |  [Aufbewahrungs-Nr](retentionid.md)  |  [RetentionPeriod](retentionperiod.md)  |  [Typ (ElcFolderType)](type-elcfoldertype.md)  |  [Aufbewahrungszeit](retentionaction.md)  |  [Beschreibung](description.md)  |  [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md)  |  [Isarchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="c4a22-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4a22-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4a22-112">Parent elements</span></span>

[<span data-ttu-id="c4a22-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="c4a22-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="c4a22-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4a22-114">Remarks</span></span>

<span data-ttu-id="c4a22-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c4a22-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c4a22-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c4a22-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4a22-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c4a22-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4a22-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4a22-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4a22-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4a22-119">Schema name</span></span>  <br/> |<span data-ttu-id="c4a22-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c4a22-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4a22-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4a22-121">Validation file</span></span>  <br/> |<span data-ttu-id="c4a22-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4a22-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4a22-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c4a22-123">Can be empty</span></span>  <br/> ||
   

