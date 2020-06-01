---
title: User Mailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: Das UserMailbox -Element identifiziert ein Benutzerpostfach.
ms.openlocfilehash: 9bb1b08320f5e6f4843383a8e3aff96fc3dcccad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465317"
---
# <a name="usermailbox"></a><span data-ttu-id="f76e2-103">User Mailbox</span><span class="sxs-lookup"><span data-stu-id="f76e2-103">UserMailbox</span></span>

<span data-ttu-id="f76e2-104">Das **UserMailbox** -Element identifiziert ein Benutzerpostfach.</span><span class="sxs-lookup"><span data-stu-id="f76e2-104">The **UserMailbox** element identifies a user mailbox.</span></span> 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 <span data-ttu-id="f76e2-105">**UserMailboxType**</span><span class="sxs-lookup"><span data-stu-id="f76e2-105">**UserMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f76e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f76e2-106">Attributes and elements</span></span>

<span data-ttu-id="f76e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f76e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f76e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f76e2-108">Attributes</span></span>

|<span data-ttu-id="f76e2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f76e2-109">**Attribute**</span></span>|<span data-ttu-id="f76e2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f76e2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f76e2-111">Id</span><span class="sxs-lookup"><span data-stu-id="f76e2-111">Id</span></span>  <br/> |<span data-ttu-id="f76e2-112">Der Textwert des **Id** -Attributs ist der Bezeichner des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="f76e2-112">The text value of the **Id** attribute is the identifier of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="f76e2-113">IsArchive</span><span class="sxs-lookup"><span data-stu-id="f76e2-113">IsArchive</span></span>  <br/> |<span data-ttu-id="f76e2-p101">Der Textwert der **IsArchive** -Attribut gibt an, ob das Postfach ein Archivpostfach ist. Der Textwert **true** für das **IsArchive** -Attribut gibt an, dass das Postfach ein Archivpostfach ist. Der Wert **false** für das **IsArchive** -Attribut gibt an, dass das Postfach eines primären Postfachs ist.  </span><span class="sxs-lookup"><span data-stu-id="f76e2-p101">The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox. A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox. A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.  </span></span><br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f76e2-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f76e2-117">Child elements</span></span>

<span data-ttu-id="f76e2-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="f76e2-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f76e2-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f76e2-119">Parent elements</span></span>

<span data-ttu-id="f76e2-120">[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="f76e2-120">[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f76e2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f76e2-121">Remarks</span></span>

<span data-ttu-id="f76e2-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f76e2-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f76e2-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f76e2-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f76e2-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f76e2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f76e2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f76e2-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f76e2-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f76e2-126">Schema name</span></span>  <br/> |<span data-ttu-id="f76e2-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f76e2-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f76e2-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f76e2-128">Validation file</span></span>  <br/> |<span data-ttu-id="f76e2-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f76e2-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f76e2-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f76e2-130">Can be empty</span></span>  <br/> |<span data-ttu-id="f76e2-131">true</span><span class="sxs-lookup"><span data-stu-id="f76e2-131">true</span></span>  <br/> |
   

