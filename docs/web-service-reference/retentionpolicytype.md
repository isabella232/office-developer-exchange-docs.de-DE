---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: Das RetentionPolicyType-Element gibt den Aufbewahrungs Richtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird.
ms.openlocfilehash: 3900718f10e1e11d5864ebf7e64a3e1e22aa45c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462871"
---
# <a name="retentionpolicytype"></a><span data-ttu-id="1f8ff-103">RetentionPolicyType</span><span class="sxs-lookup"><span data-stu-id="1f8ff-103">RetentionPolicyType</span></span>

<span data-ttu-id="1f8ff-104">Das **RetentionPolicyType** -Element gibt den Aufbewahrungs Richtlinientyp an, der auf Elemente in einer Unterhaltung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-104">The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation.</span></span> 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 <span data-ttu-id="1f8ff-105">**RetentionType**</span><span class="sxs-lookup"><span data-stu-id="1f8ff-105">**RetentionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f8ff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f8ff-106">Attributes and elements</span></span>

<span data-ttu-id="1f8ff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f8ff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f8ff-108">Attributes</span></span>

<span data-ttu-id="1f8ff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f8ff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f8ff-110">Child elements</span></span>

<span data-ttu-id="1f8ff-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f8ff-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f8ff-112">Parent elements</span></span>

[<span data-ttu-id="1f8ff-113">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="1f8ff-113">ConversationAction</span></span>](conversationaction.md)
  
## <a name="text-value"></a><span data-ttu-id="1f8ff-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f8ff-114">Text value</span></span>

<span data-ttu-id="1f8ff-115">Der Textwert des **RetentionPolicyType** -Elements ist der Aufbewahrungs, der auf Elemente in einer Unterhaltung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-115">The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation.</span></span> <span data-ttu-id="1f8ff-116">Der Textwert von **Delete** gibt an, dass die Elemente in der Unterhaltung gelöscht werden, wenn die Aufbewahrungsdauer abläuft.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-116">The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires.</span></span> <span data-ttu-id="1f8ff-117">Der Textwert von **Archive** gibt an, dass die Elemente in der Unterhaltung nach Ablauf der Aufbewahrungsdauer in das Archivpostfach verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-117">The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f8ff-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f8ff-118">Remarks</span></span>

<span data-ttu-id="1f8ff-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1f8ff-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f8ff-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1f8ff-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f8ff-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f8ff-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f8ff-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f8ff-123">Schema name</span></span>  <br/> |<span data-ttu-id="1f8ff-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1f8ff-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f8ff-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f8ff-125">Validation file</span></span>  <br/> |<span data-ttu-id="1f8ff-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f8ff-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f8ff-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1f8ff-127">Can be empty</span></span>  <br/> ||
   

