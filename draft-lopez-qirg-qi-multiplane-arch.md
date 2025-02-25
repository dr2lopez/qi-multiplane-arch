---
title: "A Multiplane Architecture Proposal for the Quantum Internet"
abbrev: "qi-multiplane-arch"
category: info
docname: draft-lopez-qirg-qi-multiplane-arch-latest
submissiontype: IRTF
number:
date:
consensus: true
v: 3
area: "IRTF"
workgroup: "Quantum Internet Research Group"
keyword:
 - quantum
 - architecture
 - QKD
 - CLAS
venue:
  group: "Quantum Internet Research Group"
  type: "Research Group"
  mail: "qirg@irtf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/qirg/"
  github: "dr2lopez/qi-multiplane-arch"
  latest: "https://dr2lopez.github.io/qi-multiplane-arch/draft-lopez-qirg-qi-multiplane-arch.html"
author:
 - name: Diego Lopez
   organization: Telefonica
   email: "diego.r.lopez@telefonica.com"
 - name: Vicente Martin
   organization: UPM
   email: "vicente.martin@upm.es"
 - name: Blanca Lopez
   organization: IMDEA Networks
   email: "blanca.lopez@imdea.org"
 - name: Luis M. Contreras
   organization: Telefonica
   email: "luismiguel.contrerasmurillo@telefonica.com"

normative:
 RFC8597:
informative:
 QTTI21:
  title: "Quantum Technologies in the Telecommunications Industry"
  author:
  - name: Vicente Martin
  - name: Juan Pedro Brito
  - name: Carmen Escribano
  - name: Marco Menchetti
  - name: Catherine White
  - name: Andrew Lord
  - name: Felix Wissel
  - name: Matthias Gunkel
  - name: Paulette Gavignet
  - name: Naveena Genay
  - name: Olivier Le Moult
  - name: Carlos Abellan
  - name: Antonio Manzalini
  - name: Antonio Pastor-Perales
  - name: Victor Lopez
  - name: Diego Lopez
  date: July 2021
  target: https://epjquantumtechnology.springeropen.com/articles/10.1140/epjqt/s40507-021-00108-9
 RFC9340:
 QUCS: I-D.irtf-qirg-quantum-internet-use-cases
 QIPS22:
  title: "Quantum Internet Protocol Stack: a Comprehensive Survey"
  author:
  - name: Jessica Illiano
  - name: Marcello Caleffia
  - name: Antonio Manzalini
  - name: Angela Sara Cacciapuoti
  date: Augut 2022
  target: https://www.sciencedirect.com/science/article/abs/pii/S1389128622002250
 Y3802:
  title: "ITU-T Recommendation Y.3802: Quantum key distribution networks. Functional architecture"
  date: April 2021
  target: https://www.itu.int/rec/T-REC-Y.3802
 MADQCI23:
  title: "The Madrid Testbed: QKD SDN Control and Key Management in a Production Network"
  author:
  - ins: V. Martin
  - ins: J.P. Brito
  - ins: L. Ortíz
  - ins: R. Brito-Méndez
  - ins: R. Vicente
  - ins: J. Saez-Buruaga
  - ins: A.J. Sebastian
  - ins: D.G. Aguado
  - ins: M.I. García-Cid
  - ins: J. Setien
  - ins: P. Salas
  - ins: C. Escribano
  - ins: E. Dopazo
  - ins: J. Rivas-Moscoso
  - ins: A. Pastor-Perales
  - ins: D. Lopez
  date: July 2023
  target: https://ieeexplore.ieee.org/document/10207295
 EUROQCI:
  title: "The European Quantum Communication Infrastructure (EuroQCI) Initiative"
  date: September 2023
  target: https://digital-strategy.ec.europa.eu/en/policies/european-quantum-communication-infrastructure-euroqci
 PSQN22:
  title: "Packet switching in quantum networks: A path to the quantum Internet"
  author:
  - name: Stephen DiAdamo
  - name: Bing Qi
  - name: Glen Miller
  - name: Ramana Kompella
  - name: Alireza Shabani
  date: October 2022
  target: https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.4.043064
 ETSI04:
  title: "ETSI GS QKD 004: Quantum Key Distribution (QKD); Application Interface"
  date: August 2020
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/004/02.01.01_60/gs_QKD004v020101p.pdf
 ETSI14:
  title: "ETSI GS QKD 014: Quantum Key Distribution (QKD); Protocol and data format of REST-based key delivery API"
  date: February 2019
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/014/01.01.01_60/gs_qkd014v010101p.pdf
 ETSI15:
  title: "ETSI GS QKD 015: Quantum Key Distribution (QKD); Control Interface for Software Defined Networks"
  date: April 2022
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/015/02.01.01_60/gs_QKD015v020101p.pdf
 ETSI18:
  title: "ETSI GS QKD 018: Quantum Key Distribution (QKD); Orchestration Interface for Software Defined Networks"
  date: April 2022
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/018/01.01.01_60/gs_QKD018v010101p.pdf
 NFV06:
  title: "ETSI GS NFV 006: Network Functions Virtualisation (NFV) Release 4; Management and Orchestration; Architectural Framework Specification"
  date: December 2022
  target: https://www.etsi.org/deliver/etsi_gs/NFV/001_099/006/04.04.01_60/gs_NFV006v040401p.pdf
 EVCKMM:
  title: "An Enhanced Virtualized Control and Key Management Model for QKD Networks"
  author:
  - name: Blanca Lopez
  - name: Ivan Vidal
  - name: Francisco Valera
  - name: Diego Lopez
  date: January 2025
  target: https://ieeexplore.ieee.org/document/10870375
 FIQNSA:
  title: "Unleashing Flexibility and Interoperability in QKD Networks: The Power of Softwarized Architectures"
  author:
  - name: Blanca Lopez
  - name: Ivan Vidal
  - name: Francisco Valera
  - name: Diego Lopez
  - name: Antonio Pastor
  date: July 2024
  target: https://ieeexplore.ieee.org/document/10628345
 CLASEVO: I-D.contreras-coinrg-clas-evolution
 QIROAD18:
  title: "Quantum internet: A vision for the road ahead"
  author:
  - name: Stephanie Wehner
  - name: David Elkouss
  - name: Ronald Hanson
  date: October 2018
  target: https://doi.org/10.1126/science.aam9288
 QKNDT24:
  title: "Service for Deploying Digital Twins of QKD Networks"
  author:
  - name: Raul Martin
  - name: Blanca Lopez
  - name: Ivan Vidal
  - name: Francisco Valera
  - name: Borja Nogales
  date: January 2024
  target: https://doi.org/10.3390/app14031018


--- abstract

A consistent reference architecture model for the Quantum Internet is required to progress in its evolution, providing a framework for the integration of the protocols applicable to it, and enabling the advance of the applications based on it. This model has to satisfy three essential requirements: agility, so it is able to adapt to the evolution of quantum communications base technologies, sustainability, with open availability in technological and economical terms, and pliability, being able to integrate with the operations and management procedures in current networks. This document proposes such an architecture framework, with the goal of providing a conceptual common framework for the integration of technologies intended to build the Quantum Internet infrastructure and its integration with the current Internet. The framework is based on the already extensive experience in the deployment of QKD network infrastructures and on related initiatives focused on the integration of network infrastructures and services.

--- middle

# Introduction

As another case of the "classical vs quantum" apparent contradictions, the nature of quantum communications {{QTTI21}}, associated with natural physical effects that require a specific infrastructure to be used for communications, poses a significant challenge in the definition of any network reference architecture to be used for such communications. Nevertheless, the growing interest on quantum networking, its applications, and the eventual availability of a Quantum Internet, require of consensus on an architecture framework able to support the definition and evolution of different protocols and interfaces.

Several steps have been taken in this direction, including the identification of architectural principles and base technologies made in {{RFC9340}}, the description of relevant use cases {{QUCS}}, and specific approaches to layered models for Quantum Networking, summarized and discussed in {{QIPS22}}. While the principles provide an extremely valuable common ground for further collaboration among quantum and network practitioners, they are not intended to provide the solid framework required for progressing in the definition of specific protocols and other interfaces for common network management tasks and interactions with user applications. On the other hand, the proposals made for a layered approach provide interesting insights on requirements and potential mechanisms to structure quantum communications, but, first, they do not include essential aspects for a network at scale and, second and most important, they do not take into account the need for direct interactions beyond the layered structure, such as those between classical and quantum networking services, between applications and the quantum network, etc.

In parallel, the operational experience with the first kind of infrastructures using quantum communication technologies to provide an actual network service, those focused on Quantum Key Distribution (QKD), has allowed practitioners to explore the solution space and identify design patterns that seem applicable to the general case of a Quantum Internet. A corpus of architectural proposals {{Y3802}}, experimental deployments {{MADQCI23}} and pilot infrastructures {{EUROQCI}} have become available in the recent years, and can be used to derive useful conclusions, especially if combined with recent proposals in network architecture {{RFC8597}}, intended to address the complexity of management and integration at scale beyond the basic layered constructs supporting connectivity.

This document proposes a multi-plane reference architecture for the Quantum Internet, derived from available proposals and the operational experience with QKD infrastructure. The proposal attempts to define a framework with three essential properties to guarantee a seamless evolution of the technology, and the consolidation of applications and management practices:

* Agility: Provide abstractions able to incorporate new protocols and interfaces as the technology evolves, avoiding a tight coupling with specific physical technologies.

* Sustainability: Considering it at all levels and in full scale, especially regarding environmental and social impacts, including open availability in technological and economical terms, and fostering infrastructure reuse.

* Pliability: Facilitate the seamless integration of classical and quantum network operational procedures, applying and adapting best practices in use by the Internet community.

And trying to address three essential characteristics already identified in {{PSQN22}}:

* Universality, so a quantum network can accommodate any application.

* Transparency, so quantum networks can share physical media with classical networks.

* Scalability, so quantum networking protocols can support the growth of the network.


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Base Technologies: QKD Experience and Evolved SDN Concepts

The design and deployment of QKD infrastructures has followed a number of design principles, based on the best practices in network architecture and management established during the lifetime of the Internet (and even before), and focused on the separation of concerns, that have been converging on the trends around open disaggregation strategies, and the identification of separate data and control planes, connected by means of open interfaces.

In what relates to the evolution of SDN concepts, the Cooperating Layered Architecture for Software-Defined Networking (CLAS) {{RFC8597}} described a SDN architecture structured in two different strata, namely Service Stratum and Transport Stratum.  On one hand, the Service Stratum contains the functions related to the provision of services and the capabilities offered to external applications. On the other hand, the Transport Stratum comprises the functions focused on the transfer of data between the communication endpoints, e.g., between end-user devices, between two service gateways, etc.

## A QKD Multi-Plane Architecture

Applying the SDN and disaggregation principles, QKD infrastructures have been essentially structured around three different planes {{QTTI21}}. While we are not talking about a rigid, layered structure, where a given layer can only provide services to the immediate upper layer and consume services from the immediate lower layer, it is worth noting that interactions among elements in the different planes must use well-defined interfaces {{ETSI04}} {{ETSI14}} {{ETSI15}} {{ETSI18}}, and these interactions may incorporate a layered approach.

In this approach, the Quantum Forwarding Plane (QFP) is in charge of performing the operations (quantum and classical) to ensure the forwarding of the quantum signals or enable the utilization of persistent quantum resources, like persistent, distributed  entanglement. In QKD, the QFP encapsulates all the functionality required to obtain an end-to-end secret key across the network. This implies the transmission of the quantum signals and the execution of any associated protocols. Note this would require the use of classical procedures, either via a separated physical "classical channel" {{QTTI21}} or the reuse of a common channel, as proposed in "packet-oriented" approaches {{PSQN22}}. In this sense, the forwarding of the keys at intermediate nodes in the multi-hop chains used to overcome current limitations in propagation of quantum signals or states, has to be considered part of the QFP, since it is done exclusively on behalf of the QKD functionality.

On its side, the Service Overlay Plane (SOP) supports the use of the keys derived from the QFP by applications. This includes the storage, identification, delivery, and lifecycle management of the units of consumption (keys of different length, delivered according to specific patterns) at the endpoints of the network. All network functionalities at this plane can be considered application-oriented, with a clear mapping to an overlay data plane in a classical network, though the SOP elements should be aware of the nature and specific needs of the QFP they interact with. Key management mechanisms, beyond key forwarding by intermediate nodes, fit within the SOP. This comprises methods such as hybridization and augmentation techniques, or the means for synchronizing key identifiers across API boundaries.

Finally, the Control and Management Plane (CMP) is made of the elements that create and supervise the state of the network. This decoupling between network configuration and (general) data forwarding is supported by the controller, a mediation logically centralized element between the control capabilities supported by the elements in the QFP and SOP and the management and control functions. These management and control applications rely on the controller, taking advantage of the centralization it provides, to guarantee the best performance of the network and avoid diverging local control decisions that might lead to sub-optimal configurations.

It is worth noting this management centralization does not contradict the distributed principles generally applied in current networks. Local control decisions are intended to be coordinated by centralized management. While the communication between the controller and the controlled elements relies on some kind of SDN protocol, the controller exposes a consistent abstract model of the network devices and topology, that can be structured in a hierarchy of abstractions, from lower-level, element-focused ones, up to application-oriented ones.

In summary, QKD infrastructures are converging into an extended SDN model, with two differentiated data planes, controlled in a coordinated manner through a common Control and Management Plane, that supports aggregated mechanisms for further orchestration. The QFP/SOP duality constitutes a common abstract foundation for a general approach to quantum communications networks, regardless of their final purpose.

## Interfacing with Classical Networks

The interface of QKD infrastructures with classical networks (commonly identified as OTN, Optical Transport Networks) has been based on three basic principles, related to the ones we mentioned above: facilitate the reuse of physical infrastructure (sustainability and transparency), apply the abstractions commonly used in open and disaggregated networks (agility and universality), and reuse the best practices in network management being applied in current infrastructures (pliability and scalability). We can classify the interface mechanisms according to the level at which they occur.

At the application level, end-to-end key management and end-to-end key creation are obviously the main target. Since many applications of these keys are related to classical communications (direct encryption, key derivation for symmetric algorithms, peer identity…) there is a clear interface for the SOP, with classical network functions acting as consumers of the keys or, in general terms, the bit streams generated by the QFP. Further on, the application of NFV  mechanisms to any network function allows for its implementation through software virtualization techniques (virtual machines, para-virtualization containers, unikernels, etc.), irrespectively of their application environments or specific plane. The lifecycle management of all network functions, of any nature, under a common MANO stack {{NFV06}}, seems the most reasonable option.

At the control and management level, the distinct nature of network elements and the mediation nature of the controller role do not make advisable the use of common quantum/OTN controllers, but there are common abstractions able to support cross-interactions among controllers and management applications, especially regarding:

* Quantum management applications requiring operations on topologies and physical paths in the OTN mediated by an OTN controller.

* OTN management applications requiring operation on quantum topologies mediated by the quantum controller.

* Topology updates exchanged between quantum and OTN controllers.

* The coordination through an integrated controller (commonly referred as "orchestrator"), able to provide a common view to application network functions.

At the forwarding level, there is a radical difference between the network elements in quantum networks and OTN, and therefore interactions in data forwarding are not feasible, with only two exceptions: the possibility of sharing physical media, and the use of classical channels to support QKD algorithms, as it is the case of distillation channels in protocols like BB84. In this case, a proper control of the path and physical parameters has to be applied to minimize interferences of any nature and guarantee OTN connectivity for the quantum algorithms.

## Applying Network Virtualization Principles

Recent proposals for QKD network management have explored the use of operational models that radically leverage the virtualization of control and key management functionalities {{EVCKMM}}. These approaches pave the way for a tighter integration of quantum functionality with functions already established in state of the art classical networks, including support for user/function authentication and authorization, and support for user and function mobility, while adhering to established QKD network standards. Integrating these mechanisms enhance security measures and ensure that quantum networks can seamlessly interface with existing and future telecommunications infrastructure.

While SDN ensures higher degrees of flexibility and reconfigurability by allowing network functions to be easily modified and upgraded through software changes, virtualization enables the abstraction of hardware devices by creating virtual instances, which improves scalability, resource efficiency and allows the dynamic allocation of softwarized network functions in different locations. As quantum technology evolves, a virtualized layer for softwarized network functions significantly aids adaptation to these changes, ensuring pliability and responsiveness for seamless updates, and incorporating new mechanisms without extensive hardware modifications.

As for key exchange, current technology does not allow direct end-to-end quantum key exchange between distant nodes. Instead, key distribution must rely on trusted intermediary nodes to transmit keys hop-by-hop. A key management layer where the actions of all nodes are coordinated is needed to ensure secure and efficient key distribution. Virtualizing and decoupling key management from the physical QKD devices enhances flexibility and scalability, and supports the integration of hybrid cryptographic strategies, combining QKD and post-quantum algorithms to ensure security and performance. Additionally, it allows real-time performance monitoring, data-driven control and management, and tailored access and admission mechanisms {{FIQNSA}}.

The virtualized key management layer acts as an intermediary between the clients and the cryptographic material generating devices. This layer would have as functions both those that fall within the framework of the SOP defined in previous sections, as well as key forwarding, specific to the QFP. For the latter, each functional element of this layer, identified as key managers entities in {{EVCKMM}}, has a forwarding table, which can be dynamically updated whenever necessary by the control plane. Adittionally, they implement a token bucket for each application session, to control the request rate by limiting it to an agreed-upon value at the Quality of Service (QoS) level.

The virtualized control plane can have different functional elements, and, as with the key management layer, several instances of the same element can be executed as necessary for the correct operation of the network. Foundational elements include: a controller, an access control and an admission control component, a routing module, and a monitoring element. This set allows the execution of network access policies, ensuring that no unauthorized user or process enters the network, verifies the configuration parameters of new sessions opened by applications, ensuring that they are granted the appropriate QoS, and performs performance tests on the physical links and collecting statistics on the QKD modules, quickly alerting about any failure or possible attack on the QFP.

## CLAS and Quantum Networks

As discussed above, SDN principles have enabled the base abstractions for the conceptualization of QKD infrastructures, including the services they provide and the required interactions in the use of classical infrastructure to support the required connectivity patterns. The original CLAS archiecture, as defined by {{RFC8597}}, addresses SDN evolution considering the forwarding (transport) and service aspects in two separated but coordinated planes. This approach matches the multi-plane approach described for QKD infeastructures, though it seems somehow limited to address the required interactions with physical connectivity, as well as to incorporate general requirements regarding automation to support convergence with operational practices.

The new extension of the CLAS architecture, as defined in {{CLASEVO}}, intends to address the current evolution of networks and the services they support introducing new aspects, in particular the considerations of distributed computing capabilities attached to different points in the network, and the introduction of evidence-driven techniques, such as Analytics, Artificial Intelligence (AI) and Machine Learning (ML) to improve operations by means of closed-loop automation.

The CLAS framework provides a sound foundation for incorporating the experience gained with QKD deployments in a general proposal applicable to the Quantum Internet, as it is essentially compatible with the architectural lessons learned within the QKD fields, and at the same time supports additional degrees of freedom regarding the integration of control mechanisms, and the interplay with the (shared) infrastructure and its management.


# A Framework Architecture for the Quantum Internet

Based on the available experience on the deployment of existing QKD infrastructures and on the evolution of SDN-enabled architectures described in the previous section, this document proposes an architecture framework intended to offer a conceptual common framework for the integration of technologies intended to build the Quantum Internet infrastructure and its integration with the current Internet.

Once we presented in the  previous section the lessons learned from QKD deployments, introducing a general architecture applicable to those deployments, in this section we propose the generalization of such architecture towards a Quantum Internet, augmented by the extended SDN approach proposed by the evolved CLAS in {{CLASEVO}}. In what follows,we will discuss how this framework architecure would support the required properties: agility, allowing for technology evolution, sustainability, fostering infrastructure reuse, and pliability, supporting operational best practices.

Furthermore, we propose here a general network architecture trying to incorporate relevant trends such as cloud nativeness, the integration of zero-touch management, or the considerations about intent. With this in mind, in what follows a CLAS-based architecture frameworks for quantum communications networks is introduced, including the proposed strata and their main characteristics.


## Strata for Quantum Networks

The CLAS architecture was initially conceived from the perspective of exploiting the advantages of network programmability in operational networks, complementing and going beyond the traditional layered structured of the original SDN proposal. Following the CLAS philosophy, as proposed in its recent update {{CLASEVO}} of decoupling services, additional functionality, and base connectivity, the architecture of a quantum network should be composed of:

* A Service Stratum, dealing with the functionality related to the purpose of the quantum network, and aligned with SOP described for QKD networks above. At this moment, the most general service, beyond QKD key management, is obviously entanglement distribution in a general quantum network. Others can be considered, as time synchronization, identity assurance or sensing. The service stratum would consider the relevant service units (keys, shared states, identities, timelines...), deal with their appropriate forwarding and routing, and deliver these service units as requested by the user application functions.

* A Quantum Forwarding Stratum, in charge of the direct application of quantum protocols and algorithms between the two endpoints of a quantum link, even when it is a multi-hop one, very much as the QFP we described as part of QKD deployments.

(TBD: The term "Quantum Forwarding" seems to not gather full consensus. A proposal for a better term would be welcome!!)

* A Connectivity Stratum, taking care of providing the paths to support the quantum links used by the quantum forwarding and service strata. Typically, the connectivity stratum would be supported by OTN infrastructure, via fiber and/or open-space links, and would follow a common connectivity paradigm, specifically a circuit-based or packet-based one. While current quantum links deal with OTN infrastructure according to a  circuit-based paradigm, recent proposals are addressing the idea of "quantum packets" {{PSQN22}} and the connectivity stratum would have to deal, in general terms, with the classical headers of such packets.

This architecture, following the CLAS proposal itself, is built under the assumption that planes within and across strata communicate through well-defined, open interfaces supporting programmability, as a generalization of the common SDN architecture that defines a controller as a mediator between application and network (forwarding) devices. It includes the archetypal case of a centralized controller, but is not limited to that particular realization. These broader implications of SDN principles are among the main motivation of the original CLAS proposal in {{CLASEVO}}, and it is the main reason for using it as the base for the framework proposed by ths document.

Based on the images used to illustrate the strata proposed in {{CLASEVO}} and {{RFC8597}}, the relationship among the strata described above would be as shown in the following diagram:

~~~ ascii-art

                                    Application Functions
                                              /\
                                              ||
        +-------------------------------------||-------------+
        | Service Stratum                     ||             |
        |                                     \/             |
        |  +--------------+     ...........................  |
        |  | Telemetry Pl.|     . SDN Intelligence        .  |
        |  |              |<===>.                         .  |
        |  +-----/\-------+     .        +--------------+ .  |
        |        ||             .        |   Mgmt. Pl.  | .  |
        |        ||             .  +--------------+     | .  |
        |  +-----\/-------+     .  |  Control Pl. |-----+ .  |
        |  | Resource Pl. |     .  |              |       .  |
        |  |              |<===>.  +--------------+       .  |
        |  +--------------+     ...........................  |
        |                                /\             /\   |
        |                                ||             ||   |
        +--------------------------------||-------------||---+
                         Standard API -- || --          ||
        +--------------------------------||-----+       ||
        | Quantum Forwarding Stratum     ||     |       ||
        |                                \/     |       ||
        |  +----------+    ...................  |       ||
        |  | Telemetry|    . SDN             .  |  Std. ||
        |  | Plane    |<==>. Intelligence    .  |  API  ||
        |  +-----/\---+    .    +----------+ .  |    -- || --
        |        ||        .    | Mgmt. Pl.| .  |       ||
        |        ||        .  +----------+ | .  |       ||
        |  +-----\/---+    .  | Control  |-+ .  |       ||
        |  | Resource |    .  | Plane    |   .  |       ||
        |  | Plane    |<==>.  +----------+   .  |       ||
        |  +----------+    ...................  |       ||
        +----------------------------------/\---+       ||
                           Standard API -- || --        ||
                       +-------------------||-----------||-----+
                       | Connectivity      ||           ||     |
                       | Stratum           ||           ||     |
                       |                   \/           \/     |
                       |  +----------+    ...................  |
                       |  | Telemetry|    . SDN             .  |
                       |  | Plane    |<==>. Intelligence    .  |
                       |  +-----/\---+    .    +----------+ .  |
                       |        ||        .    | Mgmt. Pl.| .  |
                       |        ||        .  +----------+ | .  |
                       |  +-----\/---+    .  | Control  |-+ .  |
                       |  | Resource |    .  | Plane    |   .  |
                       |  | Plane    |<==>.  +----------+   .  |
                       |  +----------+    ...................  |
                       +---------------------------------------+

~~~

Essentially, this architecture model incorporates the findings from QKD deployments, and addresses the requirements for providing a general framework for quantum networks towards the Quantum Internet. It is intended to support the evolution of network base technologies, provide the degrees of freedom necessary to encompass different deployment models, and align with relevant trends in network operation, while considering the practical aspects related to classical connectivity.

The proposed architecture will address the evolution of network base technologies by providing abstractions able to accommodate to this evolution. Considering the stages analyzed in {{QIROAD18}}, the QKD deployment patterns described in the previous section already cover "Trusted Repeater Networks" and "Prepare and Measure Networks", and the general architecture proposed here is able to accommodate the more evolved stages, namely "Entanglement Distribution Networks", "Quantum Memory Networks", "Few Qubit Fault-Tolerant Networks", and "Quantum Computing Networks". As immediate examples we can consider the integration of features in the Connectivity Stratum with the other two strata to support entanglement forwarding among different locations, or the incorporation of future quantum repeaters into the Quantum Forwarding Stratum to support more ellaborated behaviors of the Service Stratum.

In addition, these network abstractions are intended to provide specific degrees of freedom for network design and deployment, through the incorporation of independent resource and control planes at each stratum. Given the control mechanisms identified as "SDN intelligence" on the diagram above are able to expose open interfaces, the approach for coordinating the different strata via mechanisms like those defined in {{ETSI18}} is totally feasible, and different aggregation patterns (multi-stratum, multi-domain...) and models (federated, hierarchical...) can be applied. These aggregation mechanisms are equally applicable in the case of telemetry data and their integration with closed-loop mechanisms for automation, in support of the required quantum network agility.

The evolved CLAS proposal in {{CLASEVO}} explicitly incorporates current trends in network automation, in whatever the flavor including AI and intent expressions. This architecture guarantees the future pliability of quantum networks, in alignment with the evolution of best practices in general network management.

Finally, by explicitly addressing the issues related to the connectivity of quantum links, the architecture considers the interactionis with any other relevant oparational aspects required for providing quantum network services. The direct integration of a stratum focused on this aspects makes the proposed architecture better aligned with the sustainability goal.

## Identification of Interfaces and Protocols

This section, TBP once there is agreement on the architecture framework, will include a discussion on the applicable and foreseen protocols and interfaces to be used for intra-stratum (SDN and telemetry, essentially) and inter-stratum (APIs and models applicable) interactions, as well as the capability exposure mechanisms to support the aggregation mechanisms mentioned above.

### The Role of Synthetic Environments

Due to the early stage of many, if not all, quantum technologies, experimenting with quantum devices and equipment can be seriously hindered by high costs and limited availabilty. This is especially true for experimentation at the scale required to validate network protocolos and inter- and intra-strata interfaces. In this context, it becomes appropriate the use of synthetic testbeds where it is feasible to emulate the deployment of quantum networks, thus enabling the execution of experiments and trials, where even potential network attacks can be analyzed without compromising the integrity of an already built quantum network or a signinficant number of physical devices. Based on the results introduced in {{QKNDT24}} for QKD networks, a characterization of such Quantum Network Digital Twin (QNDT) will support a better understanding of the properties of the different interfaces and protocols, and the applicability of the architecture proposed in this document.

A more detailed description of the features of a generalized QNDT, based on {{QKNDT24}} findings and the principles of the architecture described in this document is being produced, and will be integrated in a future version.

# Security Considerations

This section is TBP in detail, as the identification of interfaces and protocols progresses. The general considerations made in {{RFC8597}} apply, as well as an elaboration on the following points regarding:

* The requirements on mutual authentication in the channels used for quantum interactions, as they should require methods rooted at physical properties.

* Specific physical attacks related to the particular quantum mechanisms in use by the quantum forwarding stratum.

* The interaction of these physical attacks with classical attacks to the control and monitoring activities, possibly translating into a threat surface augmentation.

--- back

# Acknowledgments
{:numbered="false"}
This document is based on work partially funded by the EU Horizon Europe project QSNP (grant 101114043), the Spanish UNICO project OPENSEC (grant TSI-063000-2021-60), and the MadridQuantum–CM project (funded by the EU, NextGenerationEU, grant PRTR-C17.I1, and by the Comunidad de Madrid, Programa de Acciones Complementarias).
