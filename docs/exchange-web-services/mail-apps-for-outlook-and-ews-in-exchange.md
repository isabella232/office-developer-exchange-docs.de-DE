---
title: Outlook-Add-Ins und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: In diesem Artikel finden Sie Informationen über Outlook-Add-Ins und ihre Zusammenarbeit mit EWS in Exchange.
ms.openlocfilehash: fc004108c7f31ea6475d61f4e2cd2289b13d27f5
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353637"
---
# <a name="outlook-add-ins-and-ews-in-exchange"></a>Outlook-Add-Ins und EWS in Exchange

In diesem Artikel finden Sie Informationen über Outlook-Add-Ins und ihre Zusammenarbeit mit EWS in Exchange.

Outlook-Add-Ins bieten eine einzige Oberfläche und ein Programmiermodell, das Webstandards verwendet, mit denen Sie eine benutzerdefinierte Erfahrung für Ihre E-Mail-Benutzer erstellen können. Sie können Mail-Apps erstellen, die kontextbezogene oder hilfreiche Informationen in einen HTML5-Frame anzeigen, der in Outlook gehostet wird; eine Mail-App kann beispielsweise eine Bing-Karte mit einer hervorgehobenen Adresse anzeigen, wenn eine E-Mail eine Adresse enthält. Oder wenn ein Benutzer eine Nachricht verfasst, können in einer Mail-App mit nur einem Klick zusätzliche Informationen zum Empfänger angezeigt und eine Standardbegrüßung in die E-Mail eingefügt werden.

> [!NOTE]
> "Outlook" bezieht sich in diesem Artikel auf den Outlook-Rich-Client, Outlook RT, Outlook Web App und OWA für Geräte.

Die Mail-Apps-Schnittstelle ist Teil der JavaScript-API für Office. Mithilfe der API können Sie auf Informationen in Exchange zugreifen, um folgende Funktionen für Ihre Mail-App zu aktivieren:

- [Erkennen von Entitäten](http://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx) wie z. B. Adressen, Telefonnummern, Aufgabenvorschlägen oder Besprechungsvorschlägen in einer E-Mail

- Öffnen und Anzeigen von vorhandenen [Nachrichten](http://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx) und [Terminen](http://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx) in einer separaten Ansicht, sodass Benutzer Querverweise zwischen Informationen in einer oder mehreren Nachrichten erstellen können

- [Stellen von EWS-Anforderungen](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) an den Exchange-Server, auf dem das Postfach des Benutzers gehostet wird. Eine Mail-App kann beispielsweise eine Liste von Ordnern abrufen, sodass der Benutzer einen Ordner zum Speichern der Nachricht auswählen kann, alle Elemente in einer Unterhaltung anzeigen oder eine E-Mail-Nachricht als Junk markieren.

- [Abrufen ein Tokens](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) zur eindeutigen Identifizierung ein E-Mail-Kontos, um einmaliges Anmelden bei einem Drittanbieterdienst zu ermöglichen

- [Abrufen ein Tokens](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx), das es einem Drittanbieterdienst ermöglicht, EWS-Anforderungen im Auftrag des Benutzers durchzuführen, beispielweise um die Anlagen aus einem Element zu extrahieren oder ein Element für die weitere Verarbeitung vom Exchange-Server abzurufen

Mithilfe von Mail-Apps können Sie die Benutzeroberfläche von Outlook Web App für Ihre Benutzer anpassen; zum Anpassen des "Erscheinungsbilds" von Outlook Web App lesen Sie die folgenden Artikel im TechNet:

- [Erstellen eines Designs für Outlook Web App](http://technet.microsoft.com/de-DE/library/bb201700%28v=exchg.150%29.aspx)

- [Anpassen der Seiten für Anmeldung, Sprachauswahl und Fehler für Outlook Web App](http://technet.microsoft.com/de-DE/library/ee633483%28v=exchg.150%29.aspx)

Ihre Organisation kann Mail-Apps auf einem internen Server installieren, um den Zugriff auf autorisierte Benutzer zu beschränken; alternativ können Sie und andere Mail-App-Entwickler Mail-Apps im [Office Store](http://office.microsoft.com/store/) zum allgemeinen Verkauf veröffentlichen. Jeder Benutzer, auf dessen Gerät Outlook ausgeführt wird, kann Mail-Apps aus dem Marketplace herunterladen und diese installieren und verwenden.

Weitere Informationen zum Erstellen von Mail-Apps finden Sie in der [Dokumentation zu Outlook-Add-Ins](/outlook/add-ins/index.md) oder im Beispiel zum [Durchführen einer EWS-Anforderung](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528).

## <a name="ews-and-outlook-add-ins"></a>EWS und Outlook-Add-Ins

Sie können eine Teilmenge der EWS-Vorgänge auf dem Exchange-Server verwenden, das der Konto hostet, auf dem eine Mail-App ausgeführt wird.

Die [mailbox.makeEwsRequestAsync](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)-Funktionen ermöglichen es Ihnen, EWS-Anforderungen von Ihrer Mail-App zurück an den Server zu stellen, auf dem das Postfach des Benutzers gehostet wird. Sie erstellen den SOAP-Umschlag und die XML-Anforderung, und die **makeEwsRequestAsync** -Funktion ruft EWS mit einem Authentifizierungstoken auf, das das Postfach und die Mail-App identifiziert, die die Anforderung durchführt. Als Sicherheitsmaßnahme für das Benutzerpostfach lehnt der Exchange-Server alle Anforderungen ab, die nicht von der Mail-App oder von einem Postfach stammen, das nicht auf dem Server gehostet wird.

Wie jede andere Anwendung benötigt eine Mail-App Berechtigungen. Der Administrator muss Folgendes durchführen:

- [Gewähren von EWS-Zugriff](controlling-client-application-access-to-ews-in-exchange.md) für die Mail-App-Benutzer

- [Festlegen von "OAuthAuthentication" auf "True"](http://technet.microsoft.com/de-DE/library/aa997233%28v=exchg.150%29.aspx) im EWS-Verzeichnis des Clientzugriffsservers

Sie müssen außerdem sicherstellen, dass Ihre App die Lesen/Schreiben-Berechtigung für das Postfach im Apps für Office-[Berechtigungsmodell](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) anfordert.

Wenn diese Schritte abgeschlossen sind, kann die Mail-App eine Teilmenge der EWS-Vorgänge für Ordner und Elemente nutzen.

**Tabelle 1. EWS-Vorgänge für Ordner und Elemente, die von Mail-Apps genutzt werden können**

|**Ordnervorgänge**|**Elementvorgänge**|
|:-----|:-----|
|[CreateFolder-Vorgang](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder-Vorgang](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [GetFolder-Vorgang](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [UpdateFolder-Vorgang](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[CopyItem-Vorgang](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [CreateItem-Vorgang](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [FindConversation-Vorgang](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [GetConversationItems-Vorgang](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [GetItem-Vorgang](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [MarkAsJunk-Vorgang](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [MoveItem-Vorgang](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [SendItem-Vorgang](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [UpdateItem-Vorgang](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |

### <a name="service-callback-tokens"></a>Dienstrückruftoken

Mithilfe von Dienstrückruftoken können Mail-Apps ein Zugriffstoken an einen Drittanbieterdienst übergeben, sodass der Dienst EWS-Anforderungen an den Exchange-Server stellen kann, der das Postfach hostet. Beispielsweise kann eine Mail-App ein Dienstrückruftoken zusammen mit einer Liste von Anlagen-IDs für an eine E-Mail angefügte Bilder an einen Drittanbieterdienst übergeben. Der Dienst kann dann die Anlagen-IDs und die Rückruftoken verwenden, um eine EWS-Anforderung an den Exchange-Server des Benutzers zu stellen und die angefügten Bilder abzurufen. Mail-Apps können das Dienstrückruftoken auch mit einer Liste von Element-IDs verwenden, um E-Mail- und Terminelemente vom Exchange-Server abzurufen.

Das Dienstrückruftoken ist ein nicht transparentes Token, das der Drittanbieterdienst an die EWS-Anforderung in einem Bearer-Authentifizierungsheader anfügt. Das Token identifiziert die Mail-App und das Postfach, um die EWS-Anforderung zu schützen. Informationen zur Verwendung von Dienstrückruftoken finden Sie im Beispiel [Outlook-Add-Ins: Abrufen von Anlagen von einem Exchange-Server](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9).

## <a name="see-also"></a>Siehe auch


- [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)

- [Methode Mailbox.makeEwsRequestAsync (JavaScript-API für Office)](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)

- [Outlook-Add-Ins](https://docs.microsoft.com/de-DE/outlook/add-ins/)

- [Methode Mailbox.getUserIdentityTokenAsync (JavaScript-API für Office)](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)

- [Authentifizieren eines Outlook-Add-Ins mithilfe von Exchange-Identitätstoken](http://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)

- [Grundlegendes zu Berechtigungen bei Outlook-Add-Ins](https://docs.microsoft.com/de-DE/outlook/add-ins/understanding-outlook-add-in-permissions)

- [Set-WebServicesVirtualDirectory](http://technet.microsoft.com/de-DE/library/aa997233%28v=exchg.150%29.aspx)

- [Outlook-Add-Ins: Stellen einer EWS-Anforderung](http://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)

- [Outlook-Add-Ins: Verwenden eines Clientidentitätstokens](http://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)

- [Outlook-Add-Ins: Abrufen von Anlagen von einem Exchange-Server](http://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)
