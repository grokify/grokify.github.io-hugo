+++
author = "John Wang"
title = "Operations Glossary"
date = "2014-01-14"
tags = [
    "security",
]
url = "/operations/glossary/"
+++

As with any field, it is important to have clear terms and definitions so people can communicate clearly and effectively. This page will serve as an ongoing glossary to cover common terms in IT Operations.

The definitions for this page will be from a number of sources over time, but is currently from the following book which I’m in the process of reading: [The Visible Ops Handbook: Implementing ITIL in 4 Practical and Auditable Steps](https://www.amazon.com/Visible-Ops-Handbook-Implementing-Practical/dp/0975568612/)

## Glossary

* **Availability:** Typically stated as the ratio of the time that the system is operating within acceptable bounds divided by the total possible time.
* **Change Advisory Board/Emergency Committee (CAB/EC):** When there is an urgent or emergency change and the entire CAB cannot be convened, this is a defined smaller group of stakeholders who can review the change request and make a proper decision as to implementation. Their decision should then be reviewed when the CAB next convenes.
* **Change Success Rate (CSR):** The ration of successful changes to total changes. This metric shows the relative effectiveness of the change management process.
* **Configuration Drift:** The tendency of configurations to change over time. For example, a server’s configuration is most certinaly known when it is first released. As time goes on, patches get applied, and there is human intervention. As these changes accumulate, undocumented changes may have occurred and the actual configuration has thus “drifted” away from the known configuration.
* **Configuration Item (CI):** One discrete build that is tracked. It may be a base component that can not be further divided or an assembly made up of other configuration items. CIs can be hardware, software, documentation or a combination thereof.
* **Configuration Management Database (CMDB):** A system used to track configuration items, requests for change, work orders, errors, relationships, etc. The definition is often nebulous as the exact implementation varies across organizations. Fundamentally, it is the core system(s) that tracks all activities including service levels.
* **Defense-in-Depth:** A security strategy of using many layers of defense as opposed to relying on fewer layers, perhaps even just a single layer. The thought process is that by using layers, each provides an additional level of security should the preceding barrier be breached.
* **Definitive Software Library (DSL):** A repository of authorized software that is secure and has version control. Software may only be added or removed from the library through formal processes.
* **Detective Control:** Processes or systems that review records to determine activity. In IT, a change monitoring and reporting system that reviews configurations against known standards on a periodic basis and reports observed changes is an example of a detective control. Likewise, a manual review of a log file looking for anomalies is an example of a detective control.
* **Diff:** To create/detect a delta or “difference” between two items. Take lists “ABC” and “CDE”. The diff is “ABDE” as they are unique to each list while “C” is common in both lists.
* **Domain Name Server (DNS):** A server application used to map hostnames to Internet Protocol (IP) addresses.
* **Dynamic Host Configuration Protocol (DHCP):** A protocol that automatically communicates network configuration settings from a central host to distributed assets, which are configured to use the protocol to obtain their Internet addresses, domain name servers, gateways, etc.
* **Forward Schedule of Change (FSC):** A schedule that contains details of all changes and their proposed implementation dates. Items are added to it through the approved change control process.
* **Information Technology Infrastructure Library (ITIL):** A collection of best practices codified in seven books by the Office of Government Commerce in the UK. 
* **IT Process Institute (ITPI):** An independent research and membership organization engaged in three principle areas of activity: Ressearch, Benchmarking and the Development of prescriptive guidance fo practitioners and business executives.
* **Mean Time Between Failures (MTBF):** The average time between failures of the asset.
* **Mean Time To Repair (MTTR):** The average time it takes to restore service once an asset has failed or dropped below acceptable service levels.
* **Request For Change (RFC):** A formally submitted document, or electronic record, that identifies the relevant information surrounding the desired change.
* **Revision Control System (RCS):** An application that tracks versions of files or potentially another form of data through the use of access and check-in/check-out controls. Depending on the system, a baseline with subsequent differentials may be tracked or each new version is stored and assigned a unique ID.
* **Shelf Life/Release Shelf Life (RSL):** Defines how long a build will remain viable before becoming obsolete.
* **Standard Change:** Changes with readily known risks that are regularly made during the course of business, and whose outcomes are predictable.