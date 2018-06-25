---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: Das Element ImListMigrationCompleted gibt an, ob der Exchange-Informationsspeicher die instant messaging-Elemente von instant messaging-Clients verwendete enthält.
ms.openlocfilehash: 25f1b583b354a71958fbc8052c492726dc0eb7db
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829893"
---
# <a name="imlistmigrationcompleted"></a><span data-ttu-id="4231e-103">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="4231e-103">ImListMigrationCompleted</span></span>

<span data-ttu-id="4231e-104">Das Element **ImListMigrationCompleted** gibt an, ob der Exchange-Informationsspeicher die Instant messaging-von instant messaging-Clients verwendete Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="4231e-104">The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 <span data-ttu-id="4231e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4231e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4231e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4231e-106">Attributes and elements</span></span>

<span data-ttu-id="4231e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4231e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4231e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4231e-108">Attributes</span></span>

<span data-ttu-id="4231e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4231e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4231e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4231e-110">Child elements</span></span>

<span data-ttu-id="4231e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4231e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4231e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4231e-112">Parent elements</span></span>

[<span data-ttu-id="4231e-113">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="4231e-113">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a><span data-ttu-id="4231e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="4231e-114">Text value</span></span>

<span data-ttu-id="4231e-115">Der Textwert **true** für das Element **ImListMigrationCompleted** gibt an, dass die instant messaging-Kontakte, die mit der Exchange Store migriert wurde gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4231e-115">A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store.</span></span> <span data-ttu-id="4231e-116">Der Wert **false** gibt an, dass der Sofortnachricht-Kontakte Store nicht migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="4231e-116">A value of **false** indicates that the instant message contacts store has not been migrated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4231e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4231e-117">Remarks</span></span>

<span data-ttu-id="4231e-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4231e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4231e-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4231e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4231e-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4231e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4231e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4231e-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4231e-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4231e-122">Schema name</span></span>  <br/> |<span data-ttu-id="4231e-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4231e-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4231e-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4231e-124">Validation file</span></span>  <br/> |<span data-ttu-id="4231e-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4231e-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4231e-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4231e-126">Can be empty</span></span>  <br/> ||
   

