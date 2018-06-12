---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: Das RetentionPolicyTag-Element gibt die Aufbewahrungsrichtlinie für ein Postfach-Element.
ms.openlocfilehash: 2525f6d7a0ca583342d28dd9f4857a69b3a8c05a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831226"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="dc3f7-103">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="dc3f7-103">RetentionPolicyTag</span></span>

<span data-ttu-id="dc3f7-104">Das **RetentionPolicyTag** -Element gibt die Aufbewahrungsrichtlinie für ein Postfach-Element.</span><span class="sxs-lookup"><span data-stu-id="dc3f7-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
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

 <span data-ttu-id="dc3f7-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="dc3f7-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc3f7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc3f7-106">Attributes and elements</span></span>

<span data-ttu-id="dc3f7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc3f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc3f7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc3f7-108">Attributes</span></span>

<span data-ttu-id="dc3f7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc3f7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc3f7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc3f7-110">Child elements</span></span>

<span data-ttu-id="dc3f7-111">[DisplayName (String)](displayname-string.md) | [retentionid vom](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Typ (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Beschreibung](description.md) | [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="dc3f7-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc3f7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc3f7-112">Parent elements</span></span>

[<span data-ttu-id="dc3f7-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="dc3f7-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="dc3f7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc3f7-114">Remarks</span></span>

<span data-ttu-id="dc3f7-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dc3f7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc3f7-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dc3f7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc3f7-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc3f7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc3f7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc3f7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc3f7-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc3f7-119">Schema name</span></span>  <br/> |<span data-ttu-id="dc3f7-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dc3f7-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc3f7-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc3f7-121">Validation file</span></span>  <br/> |<span data-ttu-id="dc3f7-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc3f7-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc3f7-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dc3f7-123">Can be empty</span></span>  <br/> ||
   

