---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: Das ImListMigrationCompleted-Element gibt an, ob der Exchange-Informationsspeicher die von Instant Messaging-Clients verwendeten Chat Elemente enthält.
ms.openlocfilehash: 09f37d6e3663aab7cb98fc922f727ddd604f2acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456024"
---
# <a name="imlistmigrationcompleted"></a><span data-ttu-id="2f753-103">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="2f753-103">ImListMigrationCompleted</span></span>

<span data-ttu-id="2f753-104">Das **ImListMigrationCompleted** -Element gibt an, ob der Exchange-Informationsspeicher die von Instant Messaging-Clients verwendeten Chat Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="2f753-104">The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 <span data-ttu-id="2f753-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="2f753-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f753-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2f753-106">Attributes and elements</span></span>

<span data-ttu-id="2f753-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f753-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f753-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f753-108">Attributes</span></span>

<span data-ttu-id="2f753-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f753-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f753-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f753-110">Child elements</span></span>

<span data-ttu-id="2f753-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f753-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f753-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f753-112">Parent elements</span></span>

[<span data-ttu-id="2f753-113">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="2f753-113">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a><span data-ttu-id="2f753-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2f753-114">Text value</span></span>

<span data-ttu-id="2f753-115">Der Textwert **true** für das **ImListMigrationCompleted** -Element gibt an, dass der Instant Messaging-Kontaktspeicher zu der Exchange-Informationsspeicher migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f753-115">A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store.</span></span> <span data-ttu-id="2f753-116">Der Wert **false** gibt an, dass der Kontaktspeicher für Sofortnachrichten nicht migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f753-116">A value of **false** indicates that the instant message contacts store has not been migrated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2f753-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f753-117">Remarks</span></span>

<span data-ttu-id="2f753-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f753-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f753-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2f753-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f753-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2f753-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f753-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f753-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f753-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2f753-122">Schema name</span></span>  <br/> |<span data-ttu-id="2f753-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2f753-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f753-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2f753-124">Validation file</span></span>  <br/> |<span data-ttu-id="2f753-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f753-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f753-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2f753-126">Can be empty</span></span>  <br/> ||
   

