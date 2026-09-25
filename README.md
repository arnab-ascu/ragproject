# ragproject
RAG System

My project built a local depooyable RAG system using Docker containers, where other contianers consisted of download LLM models, each container acting as systems in a LAN to be able to provide an interface of retrievel. 
Two APIs were used to distribute workload and nginx was old for load balancing. 
Later RAPID scheduler was designed and implemented on a router alongside routing so that proper traffic distribution could be done to the two APIs. This Router in charge of distributing traffic was also deployed onto a container to make it fully deployable within a LAN while protecting the resources from internet. This ensures that if a company deployed the system, it would not be facing data breach which can be caused due to data being taken by LLM models for training or breach from external sources as the whole system in charge of working with the vector database is fully online. 
