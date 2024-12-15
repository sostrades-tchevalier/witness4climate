## Expected content of activities to be carried out 
 
### CT0 - Core techno integration #0: Integrated Framework for Impact Assessment

The benefit of this capability is to enable an autonomous or collaborative streamlined end2end Impact Assessment process. It shall be operated in an open environment, from the formalization of emissions and performance requirements, to the visualization, comparison and assessment of multiple solutions.

The Impact Assessment process is implemented in an open simulation framework such as current DLR Framework for Impact Assessment , which will be extended through the integration of open source advanced simulation tools. 
 
The Impact Assessment Framework includes already existing modules that will be integrated together. These modules aim at: (1) formalizing and verifying (as part of a V&V activity) emissions and performance requirements; (2) formulating and executing multi-expert distributed MDAO workflows for Impact Assessment (integrating partners capabilities for emissions and performance evaluations); (3) showing Impact Assessment results; (4) supporting multi-attribute trade-off and decision-making activities while assessing various solutions (e.g. characterized by different technologies).
 
### CT1 - Core techno integration #1: Encryption integration

The benefit of this capability is to enable effective and easy co-simulations between partners while preserving control Intellectual Property.

Starting from existing open source containerized simulation framework and [Scone](https://scontain.com/) capability formerly developed in  the European SecureCloud  project, we will integrate [Scone technology](https://sconedocs.github.io/multi-stakeholder-workflow/) into the Impact Assessment Framework. 
 
The needed integration work consists mainly in managing “Key rings.” This involves ensuring that each coopetitor provides a Scone key embedding the necessary settings and inputs for their components in a simulation scenario. These keys collectively form a “key ring” for the specific scenario. During the scenario run, the appropriate keys from this key ring must be provided to the correct model. Additionally, the storage and access control of keys and key rings should be managed by the cloud platform’s key management system to facilitate efficient management and configuration.
 
This integration will enable the use of encrypted computing models, license management in a standard cloud key repository, and consistent management of sets of keys associated with a scenario. Following this, we will develop both generic technical documentation and specific tutorials with aeronautic business acumen for our partners. Ultimately, it will result in an extended Impact Assessment platform with encryption capabilities.
 
### CT2 - Core techno integration #2: Edge models integration

The benefit of this capability is to enable effective integration of remote data in simulation processes for machine learning, calibration from test or in service sources, or Verification & Validation processes.

Starting from existing open source containerized simulation framework and using OSS<![if !supportFootnotes]>[1]<![endif]> [KubeEdge](https://kubeedge.io/) (or [Fledge](https://lfedge.org/projects/fledge/) for low-resource edge environments), we will integrate edge technology into a generic simulation discipline. 
 
The needed integration work consists mainly in a discipline template edge container image that includes typical database and/or IoT connector stacks. This also involves enabling dynamic selection of edge targets within the interface. Additionally, each edge environment should be equipped with a Kubernetes flavor, and the container spawning manifest should be dynamically adapted based on this flavor.
 This integration will facilitate the easy development of edge models within the edge generic discipline. Following this, we will develop both generic technical documentation and specific tutorials with aeronautic business acumen for our partners. Ultimately, it will result in an extended Impact Assessment platform with edge computing capabilities.  
<![if !supportFootnotes]>  
 
* * *
 <![endif]> 
 
<![if !supportFootnotes]>[1]<![endif]> OSS : Open Source Software
