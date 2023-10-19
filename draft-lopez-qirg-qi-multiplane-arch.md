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
  - name: V. Martin et al.
  target: https://epjquantumtechnology.springeropen.com/articles/10.1140/epjqt/s40507-021-00108-9
 RFC9340:
 QUCS: I-D.irtf-qirg-quantum-internet-use-cases
 QIPS22:
  title: "Quantum Internet Protocol Stack: a Comprehensive Survey"
  author:
  - name: J. Illiano et al.
  target: https://www.sciencedirect.com/science/article/abs/pii/S1389128622002250
 Y3802:
  title: "ITU-T Recommendation Y.3802: Quantum key distribution networks. Functional architecture"
  target: https://www.itu.int/rec/T-REC-Y.3802
 MADQCI23:
  title: "The Madrid Testbed: QKD SDN Control and Key Management in a Production Network"
  author:
  - name: V. Martin et al.
  target: https://ieeexplore.ieee.org/document/10207295
 EUROQCI:
  title: "The European Quantum Communication Infrastructure (EuroQCI) Initiative"
  target: https://digital-strategy.ec.europa.eu/en/policies/european-quantum-communication-infrastructure-euroqci
 PSQN22:
  title: "Packet switching in quantum networks: A path to the quantum Internet"
  author:
  - name: S. DiAdamo et al.
  target: https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.4.043064
 ETSI04:
  title: "ETSI GS QKD 004: Quantum Key Distribution (QKD); Application Interface"
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/004/02.01.01_60/gs_QKD004v020101p.pdf
 ETSI14:
  title: "ETSI GS QKD 014: Quantum Key Distribution (QKD); Protocol and data format of REST-based key delivery API"
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/014/01.01.01_60/gs_qkd014v010101p.pdf
 ETSI15:
  title: "ETSI GS QKD 015: Quantum Key Distribution (QKD); Control Interface for Software Defined Networks"
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/015/02.01.01_60/gs_QKD015v020101p.pdf
 ETSI18:
  title: "ETSI GS QKD 018: Quantum Key Distribution (QKD); Orchestration Interface for Software Defined Networks"
  target: https://www.etsi.org/deliver/etsi_gs/QKD/001_099/018/01.01.01_60/gs_QKD018v010101p.pdf
 NFV06:
  title: "ETSI GS NFV 006: Network Functions Virtualisation (NFV) Release 4; Management and Orchestration; Architectural Framework Specification"
  target: https://www.etsi.org/deliver/etsi_gs/NFV/001_099/006/04.04.01_60/gs_NFV006v040401p.pdf
 CLASEVO: I-D.contreras-coinrg-clas-evolution


--- abstract

A consistent reference architecture model for the Quantum Internet is required to progress in its evolution, providing a framework for the integration of the protocols applicable to it, and enabling the advance of the applications based on it. This model has to satisfy three essential requirements: agility, so it is able to adapt to the evolution of quantum communications base technologies, sustainability, with open availability in technological and economical terms, and pliability, being able to integrate with the operations and management procedures in current networks. This document proposes such an architecture framework, based on the already extensive experience in the deployment of QKD network infrastructures and related initiatives on the integration of network infrastructures and services.

--- middle

# Introduction

As another case of the "classical vs quantum" apparent contradictions, the nature of quantum communications {{QTTI21}}, associated with natural physical effects that require a specific infrastructure to be used for communications, poses a significant challenge in the definition of any network reference architecture to be used for such communications. Nevertheless, the growing interest on quantum networking, its applications, and the eventual availability of a Quantum Internet, require of consensus on an architecture framework able to support the definition and evolution of different protocols and interfaces.

Several steps have been taken in this direction, including the identification of architectural principles and base technologies made in {{RFC9340}}, the description of relevant use cases {{QUCS}}, and specific approaches to layered models for Quantum Networking, summarized and discussed in {{QIPS22}}. While the principles provide an extremely valuable common ground for further collaboration among quantum and network practitioners, they are not intended to provide the solid framework required for progressing in the definition of specific protocols and other interfaces for common network management tasks and interactions with user applications. On the other hand, the proposals made for a layered approach provide interesting insights on requirements and potential mechanisms to structure quantum communications, but, first, they do not include essential aspects for a network at scale and, second and most important, they do not take into account the need for direct interactions beyond the layered structure, such as those between classical and quantum networking services, between applications and the quantum network, etc.

In parallel, the operational experience with the first kind of infrastructures using quantum communication technologies to provide an actual network service, those focused on Quantum Key Distribution (QKD), has allowed practitioners to explore the solution space and identify design patterns that seem applicable to the general case of a Quantum Internet. A corpus of architectural proposals {{Y3802}}, experimental deployments {{MADQCI23}} and pilot infrastructures {{REF-EUROQCI}} have become available in the recent years, and can be used to derive useful conclusions, especially if combined with recent proposals in network architecture {{RF8597}}, intended to address the complexity of management and integration at scale beyond the basic layered constructs supporting connectivity.

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


# A QKD Multi-Plane Architecture

The design and deployment of QKD infrastructures has followed a number of design principles, based on the best practices in network architecture and management established during the lifetime of the Internet (and even before), and focused on the separation of concerns, that have been converging on the trends around open disaggregation strategies, and the identification of separate data and control planes, connected by means of open interfaces.

Applying these principles, QKD infrastructures are essentially structured around three different planes {{QTTI21}}. While we are not talking about a rigid, layered structure, where a given layer can only provide services to the immediate upper layer and consume services from the immediate lower layer, it is worth noting that interactions among elements in the different planes must use well-defined interfaces {{ETSI04}} {{ETSI14}} {{ETSI15}} {{ETSI18}}, and this interactions may incorporate a layered approach.

The Quantum Forwarding Plane (QFP) is in charge of performing the operations (quantum and classical) to ensure the forwarding of the quantum signals or enable the utilization of persistent quantum resources, like persistent, distributed  entanglement. In QKD, the QFP encapsulates all the functionality required to obtain an end-to-end secret key across the network. This implies the transmission of the quantum signals and the execution of any associated protocols. Note this would require the use of classical procedures, either via a separated physical "classical channel" {{QTTI21}} or the reuse of a common channel, as proposed in "packet-oriented" approaches {{PSQN22}}. In this sense, the forwarding of the keys at intermediate nodes in the multi-hop chains used to overcome current limitations in propagation of quantum signals or states, has to be considered part of the QFP, since it is done exclusively on behalf of the QKD functionality.

The Service Overlay Plane (SOP) supports the use of the keys derived from the QFP by applications. This includes the storage, identification, delivery, and lifecycle management of the units of consumption (keys of different length, delivered according to specific patterns) at the endpoints of the network. All network functionalities at this plane can be considered conventional, with a clear mapping to and overlay data plane in classical network, though the SOP elements should be aware of the nature and specific needs of the QFP they interact with.

The Control and Management Plane (CMP) is made of the elements that create and supervise the state of the network. This decoupling between network configuration and (general) data forwarding is supported by the controller, a mediation logically centralized element between the control capabilities supported by the elements in the QFP and SOP and the management and control functions. These management and control applications rely on the controller, taking advantage of the centralization it provides, to guarantee the best performance of the network and avoid diverging local control decisions that might lead to sub-optimal configurations.

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


# Introducing CLAS for Quantum Networks

The Cooperating Layered Architecture for Software-Defined Networking (CLAS) {{RFC8597}} describes a SDN architecture structured in two different strata, namely Service Stratum and Transport Stratum.  On one hand, the Service Stratum contains the functions related to the provision of services and the capabilities offered to external applications. On the other hand, the Transport Stratum comprises the functions focused on the transfer of data between the communication endpoints (e.g., between end-user devices, between two service gateways, etc.).

A new extension of the CLAS architecture {{CLASEVO}} intends to address the current evolution of networks and the services they support introducing new aspects, in particular the considerations of distributed computing capabilities attached to different points in the network, and the introduction of evidence-driven techniques, such as Analytics, Artificial Intelligence (AI) and Machine Learning (ML) to improve operations by means of closed-loop automation.

The CLAS framework provides a sound foundation for incorporating the experience gained with QKD deployments in a general proposal applicable to the Quantum Internet, as it is essentially compatible with the architectural lessons learned within the QKD fields, and at the same time supports additional degrees of freedom regarding the integration of control mechanisms, and the interplay with the (shared) infrastructure and its management. Furthermore, we are talking of a general network architecture trying to incorporate general trends such as cloud nativeness, the integration of zero-touch management, or the considerations about intent. With this in mind, in what follows a CLAS-based architecture frameworks for quantum communications networks is introduced, including the proposed strata and their main characteristics.

## CLAS Strata for Quantum Networks

Following the CLAS philosophy, as proposed in its recent update {{CLASEVO}} of decoupling services, additional function, and base connectivity, the architecture of a quantum network should be composed of:

* A Service Stratum, dealing with the functionality related to the purpose of the quantum network, and aligned with SOP described for QKD networks above. At this moment, the most feasible services are the generation of management of keys in QKD, and entanglement distribution in a general quantum network, but others can be considered, as time synchronization, identity assurance or sensing. The service stratum would consider the relevant service units (keys, shared states, identities, timelines...), deal with their appropriate forwarding and routing, and deliver these service units as requested by the user application functions.

* A Quantum Forwarding Stratum, in charge of the direct application of quantum protocols and algorithms between the two endpoints of a quantum link, even when it is a multi-hop one, very much as the QFP we described as part of QKD deployments.

* Connectivity Stratum, taking care of providing the paths to support the quantum links used by the quantum forwarding and service strata. Typically, the connectivity stratum would be supported by OTN infrastructure, via fiber and/or open-space links, and would follow a common connectivity paradigm, specifically a circuit-based or packet-based one. While current quantum links deal with OTN infrastructure according to a  circuit-based paradigm, recent proposals are addressing the idea of "quantum packets" {{PSQN22}} and the connectivity stratum would have to deal, in general terms, with the classical headers of such packets.

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

Essentially, this architecture model incorporates the findings from QKD deployments, and enhancing the current QKD approach by:

* Providing some additional degrees of freedom through the incorporation of independent resource and control planes at each stratum. Given the control mechanisms identified as "SDN intelligence" on the diagram above are able to expose open interfaces, the approach for coordinating the different strata via mechanisms like those defined in {{ETSI18}} is totally feasible, and different aggregation patterns (multi-stratum, multi-domain...) and models (federated, hierarchical...) can be applied. These aggregation mechanisms are equally applicable in the case of telemetry data and their integration with closed-loop mechanisms for automation, in support of the required quantum network agility.

* Incorporating the current trends to network automation, in whatever the flavor including AI and intent expressions, guaranteeing the future pliability of quantum networks, in alignment with the evolution of best practices in general network management.

* Explicitly addressing the issues related to the connectivity of quantum links and its interaction with the other relevant activity for providing quantum network services. The direct integration of a stratum focused on this aspects makes the proposed architecture better aligned with the sustainability goal.

## Identification of interfaces and protocols

This section, TBP once there is agreement on the architecture framework, will include a discussion on the applicable and foreseen protocols and interfaces to be used for intra-stratum (SDN and telemetry, essentially) and inter-stratum (APIs and models applicable) interactions, as well as the capability exposure mechanisms to support the aggregation mechanisms mentioned above.

# Security Considerations

This sections is TBP, as the identification of interfaces and protocols progresses. The general considerations made in {{RFC8597}} apply, as well as an elaboration on the following points regarding:

* The requirements on mutual authentication in the channels used for quantum interactions, as they should require methods rooted at physical properties.

* Specific physical attacks related to the particular quantum mechanisms in use by the quantum forwarding stratum.

* The interaction of these physical attacks with classical attacks to the control and monitoring activities, possibly translating into a threat surface augmentation.

--- back

# Acknowledgments
{:numbered="false"}
This document is based on work partially funded by the EU Horizon Europe project QSNP (grant 101114043), the Spanish UNICO project OPENSEC (grant TSI-063000-2021-60), and the MadridQuantum–CM project (funded by the EU, NextGenerationEU, grant PRTR-C17.I1, and by the Comunidad de Madrid, Programa de Acciones Complementarias).
