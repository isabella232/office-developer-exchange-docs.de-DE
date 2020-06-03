---
title: Postfach (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: Das Mailbox-Element enthält die Postfach-ID und die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Benutzers.
ms.openlocfilehash: 4dc5ee45c00945c30a699daa0158c96679189ab1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463895"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="1185b-103">Postfach (PreviewItemMailboxType)</span><span class="sxs-lookup"><span data-stu-id="1185b-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="1185b-104">Das **Mailbox** -Element enthält die Postfach-ID und die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1185b-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="1185b-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="1185b-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1185b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1185b-106">Attributes and elements</span></span>

<span data-ttu-id="1185b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1185b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1185b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1185b-108">Attributes</span></span>

<span data-ttu-id="1185b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1185b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1185b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1185b-110">Child elements</span></span>

<span data-ttu-id="1185b-111">[Post Fach-Nr](mailboxid.md)  |  [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="1185b-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1185b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1185b-112">Parent elements</span></span>

[<span data-ttu-id="1185b-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="1185b-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="1185b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1185b-114">Remarks</span></span>

<span data-ttu-id="1185b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1185b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1185b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1185b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1185b-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1185b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1185b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1185b-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1185b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1185b-119">Schema name</span></span>  <br/> |<span data-ttu-id="1185b-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1185b-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1185b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1185b-121">Validation file</span></span>  <br/> |<span data-ttu-id="1185b-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1185b-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1185b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1185b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1185b-124">False</span><span class="sxs-lookup"><span data-stu-id="1185b-124">false</span></span>  <br/> |
   

