---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: Das UserMailbox -Element identifiziert ein Benutzerpostfach.
ms.openlocfilehash: 9f359a2b0ba315c236d4bf189c3de321417bd390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839449"
---
# <a name="usermailbox"></a><span data-ttu-id="13a76-103">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="13a76-103">UserMailbox</span></span>

<span data-ttu-id="13a76-104">Das **UserMailbox** -Element identifiziert ein Benutzerpostfach.</span><span class="sxs-lookup"><span data-stu-id="13a76-104">The **UserMailbox** element identifies a user mailbox.</span></span> 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 <span data-ttu-id="13a76-105">**UserMailboxType**</span><span class="sxs-lookup"><span data-stu-id="13a76-105">**UserMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13a76-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13a76-106">Attributes and elements</span></span>

<span data-ttu-id="13a76-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13a76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13a76-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13a76-108">Attributes</span></span>

|<span data-ttu-id="13a76-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="13a76-109">**Attribute**</span></span>|<span data-ttu-id="13a76-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13a76-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13a76-111">Id</span><span class="sxs-lookup"><span data-stu-id="13a76-111">Id</span></span>  <br/> |<span data-ttu-id="13a76-112">Der Textwert des **Id** -Attributs ist der Bezeichner des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="13a76-112">The text value of the **Id** attribute is the identifier of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="13a76-113">IsArchive</span><span class="sxs-lookup"><span data-stu-id="13a76-113">IsArchive</span></span>  <br/> |<span data-ttu-id="13a76-p101">Der Textwert der **IsArchive** -Attribut gibt an, ob das Postfach ein Archivpostfach ist. Der Textwert **true** für das **IsArchive** -Attribut gibt an, dass das Postfach ein Archivpostfach ist. Der Wert **false** für das **IsArchive** -Attribut gibt an, dass das Postfach eines primären Postfachs ist.  </span><span class="sxs-lookup"><span data-stu-id="13a76-p101">The text value of the **IsArchive** attribute indicates whether the mailbox is an archive mailbox. A text value of **true** for the **IsArchive** attribute indicates that the mailbox is an archive mailbox. A value of **false** for the **IsArchive** attribute indicates that the mailbox is a primary mailbox.  </span></span><br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13a76-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13a76-117">Child elements</span></span>

<span data-ttu-id="13a76-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="13a76-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13a76-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13a76-119">Parent elements</span></span>

<span data-ttu-id="13a76-120">[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="13a76-120">[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13a76-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13a76-121">Remarks</span></span>

<span data-ttu-id="13a76-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="13a76-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="13a76-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="13a76-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13a76-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13a76-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13a76-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="13a76-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13a76-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13a76-126">Schema name</span></span>  <br/> |<span data-ttu-id="13a76-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="13a76-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="13a76-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13a76-128">Validation file</span></span>  <br/> |<span data-ttu-id="13a76-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13a76-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13a76-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="13a76-130">Can be empty</span></span>  <br/> |<span data-ttu-id="13a76-131">true</span><span class="sxs-lookup"><span data-stu-id="13a76-131">true</span></span>  <br/> |
   

