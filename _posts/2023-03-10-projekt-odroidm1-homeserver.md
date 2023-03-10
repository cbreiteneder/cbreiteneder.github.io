---
layout: post
title: "Projekt: Energieeffizienter ODROID-M1 Homeserver"
description: Konfigurations eines neuen energieeffizienten Heimservers
date: 2023-03-10 15:00:00 +0100
tags: Homeserver
---
Aufgrund der aktuellen Lage am Energiemarkt hab ich mir für das Jahr 2023 vorgenommen mein Heimnetzwerk so energieeffizient wie möglich zu gestalten.

Bis dato war eine Synology DS218+ mit einer VM und vier Docker-Containern als Homeserver im Einsatz. Die Synology hat im Idle ungefähr 20 Watt verbraucht, das sollte auf jeden Fall effizienter gehen. 

Nach einiger Recherche bin ich auf den [ODROID-M1](https://www.hardkernel.com/shop/odroid-m1-with-8gbyte-ram/) von Hardkernel gestoßen. Der ODROID-M1 ist ein Einplatinencomputer, der für den Einsatz in einer Vielzahl von Embedded-System-Anwendungen entwickelt wurde.  

### Hardware
Für den Homeserver habe ich mich für die folgenden Komponenten entschieden:  
  
| Komponente | Kaufpreis | Link |
|--|--|--|
| ODROID-M1 mit 8 GB RAM | € 129,95 | <https://www.pollin.de/p/odroid-m1-einplatinen-computer-8-gb-ram-811475> |
| ODROID-M1 SATA-Montageset | €12,95 | <https://www.pollin.de/p/odroid-m1-sata-montageset-811479> |
| QuatPower Stecker-Schaltnetzteil  | € 8,95 | <https://www.pollin.de/p/quatpower-stecker-schaltnetzteil-xy24se-120200vq-ew55-21-12v-2-0a-5-5-2-1-352938> |
| Samsung 980 500 GB NVMe SSD M.2   | € 65,99 | <https://www.conrad.at/de/p/samsung-980-500-gb-interne-m-2-pcie-nvme-ssd-2280-m-2-nvme-pcie-3-0-x4-retail-mz-v8v500bw-2356600.html> |
| **Summe** | **€ 217,84** | |

Als zusätzliche Datenfestplatter werde ich eine 4TB Festplatte von einer externen Seagate Portable Drive ausbauen und in den Homeserver einbauen. 

Ein passendes Gehäuse werde ich selber mit meinem 3D-Drucker produzieren. 

### Geplante Software
Als Betriebssysteme möchte ich Ubuntu Server 22.04.2 LTS installieren und die folgenden Services als Docker-Container installieren:

 - [AdGuard Home](https://adguard.com/de/adguard-home/overview.html): Blockierung von Werbung und Tracking auf DNS-Ebene (ähnlich PiHole)
 - [Paperless-ngx](https://github.com/paperless-ngx/paperless-ngx): Dokumentenverwaltung für alle elektronischen bzw. eingescannten Schriftstücker (Rechnungen, Kontoauszüge, Briefe, etc.)
 - [Home Assistant](https://www.home-assistant.io/): Quelloffene Software zur Hausautomation, es besteht somit keine Abhängigkeit von einem Anbieter und es stehen mehr als 2200 Integrationen zu verschiedenen IoT-Technologien zur Verfügung. 
 - [Unifi Controller](https://www.ui.com/): Verwaltungssoftware für die installierten Accesspoints im Haus
 - [metube](https://github.com/alexta69/metube): Weboberfläche für youtube-dl zum einfachen Download von Videos

Die Services waren auch schon auf der Synology im Betrieb, weshalb ich versuchen werde die bestehenden Daten zu übernehmen.

Soviel zu einer groben Beschreibung meines Projektes, beim nächsten Eintrag werde ich mich dem Zusammenbau und der Installation des Betriebssystems widmen. 
